## Git
### Git Nedir?
Git açık kaynak kodlu, dağıtık mimariye sahip bir [versiyon kontrol sistemidir](https://medium.com/@furkanalaybeg/versiyon-kontrol-sistemi-nedir-2f47bb830064). 

### Git kurulumu
* Git for Win >> [Download](https://git-scm.com/download/win)
* Git for Mac >> [Download](https://sourceforge.net/projects/git-osx-installer/files/) ya da ```hombrew``` kuruluysa ```brew install git``` \
<br></br>
Kurulum tamamlandıktan sonra:
* Terminal açılır ve ``` git --version``` ile kurulum kontrol edilir. 
* Local'de çalışmak için git ayarları yapılır.

	* ``` git config --global user.name "Tercihen github kullanıcı adı" ```
	* ``` git config --global user.email "github'a kayıtlı mail" ```

### Temel Komutlar
```
git config user.name # kullanıcı adını gösterir
git config user.email # kullanıcı mailini gösterir
```

#### clone
Bir projeyi kendi bilgisayarınıza kopyalamak için kullanılır.
```
git clone https://github.com/x/proje.git
```

#### init
Yeni bir repo oluşturmanıza yarar. Git için gerekli dosyaları oluşturur (initialize). 

```git init```

#### status
Dosyaların durumunu gösterir(tracked, untracked, staged, modified gibi).

#### pull
Çalışılan repo bilgilerini ve son değişiklikleri lokal branch'e çeker ve *merge* ile birleştirir. 

#### fetch
Çalışılan repo bilgilerini günceller.

#### add
Dosyaların durumunu staged yapar. Commit öncesi gereklidir. 
``` 
git add . # dizindeki tüm dosyaları ekler
git add readme.md # sadece ilgili dosyayı ekler 
```

#### commit 
Yapılan tüm değişiklikleri işler (commit). Böylece push ile repository'e gönderilecek hale getirir. Her bir commit hash'lenerek saklanır böylece yapılan işlemler hash adresi üzerinden takip edilebilir.
``` 
git commit -m "commit mesajı"
git commit -m "bug-1782 kodlu sorunun çözümü: istek geldiğinde değişkenler artık büyükten küçüğe sıralanıyor" 
```

#### push
Yapılan değişikliklerin uzak sunucuya (remote) gönderilmesini sağlayan komut. 

```git push origin master # uzak sunucudaki master branch'ine gönderir``` \
``` git push # varsayılan branch ne ise ona gönderir``` \
``` git push origin bugfix-158 # bugfix-158 branch'ine gönderir ``` 

#### branch
Yeni bir branch oluşturmak, listelemek ve silmek için kullanılır.

``` 
git branch -a # branch'leri listeler 
git branch --all
git branch yeni-branch # yeni-branch adında branch oluşturur
git branch -d yeni-branch # yeni-branch'i siler 
```

#### checkout
Branch'ler arası geçiş için kullanılır. 
``` git checkout yeni-branch ```

#### diff

Commit'ler arasındaki farkları görmek için kullanılır

#### log
Commit log'larını gösterir.


### Git for Data Science
[Github Guide](https://guides.github.com/) \
[Introduction to Git for Data Science](https://github.com/datacamp/courses-introduction-to-git-for-data-science) \
[git - basit rehber](https://rogerdudler.github.io/git-guide/index.tr.html)

 * Neden Git?
 	* Versiyonlama
 	* Canlı vb. ortamlara çıkış için kod kontrolü ve yazılımcılar ile entegre çalışabilme
 	* Kişisel projeler için portfolyö oluşturma
 * Neler bilmek gerekli?
 	* Github üzerinden repo oluşturma
 	* Branch yapısı
 	```
 	git branch my-branch # my-brach adında branch oluşturur
	git checkout my-branch # aktif branch'i my-branch yapar
	```
 	* Pull/Push/Clone
 	```
 	git pull # hali hazırda bilgisayarda olan bir git klasörünü remote (github) ile senkronize eder. 
 	git push # remote'a commit'leri gönderir.
 	git clone github.com/user/repo.git # git reposunu bilgisayara indirir.
 	```
 	* Pull Requests
 		* Bir projeye sonradan yapılan eklemeler. Birden çok kişi çalışalan projelerde kişilerin master branch'ine kendi geliştirmelerini çıkma metotları.
 		* [Örnek](https://yangsu.github.io/pull-request-tutorial/)


## Kaynaklar
* [stk.bilgi.edu.tr/media/uploads/2015/01/12/git101.pdf](https://stk.bilgi.edu.tr/media/uploads/2015/01/12/git101.pdf)
* [www.gitbook.com/book/aliozgur/git101](https://www.gitbook.com/book/aliozgur/git101)
* [ohshitgit.com](https://ohshitgit.com)
* [GitHub for Data Scientists](https://www.linkedin.com/learning/github-for-data-scientists)