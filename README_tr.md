Git Komutları
============

## Translated Versions
- [Versão em português](READMEpt.md)

___

_Sık sık kullandığım Git komutlarının listesi_

*Eğer Git aliases ile ilgileniyorsanız, `.bash_profile`, ile ilgili olan yazımı da inceleyin; https://github.com/joshnh/bash_profile/blob/master/.bash_profile*

--

### Proje alma/çekme ve oluşturma

| Komut | Açıklama |
| ----- | -------- |
| `git init` | Yerel klasör dizinine **git'i entegre et** veya **git'i proje dizinine kur** |
| `git clone ssh://git@github.com/[kullaniciadi]/[proje-adi].git` | Uzak sunucudaki projeyi lokal'e kopyala |

### Basit Snapshot'lar

| Komut | Açıklama |
| ----- | -------- |
| `git status` | Durumu kontrol et |
| `git add [dosya-adi.txt]` | Temel git akışına/bekleme bölgesine dosyayı ekle. (Bu snapshot almak için özhazırlıktır.)  |
| `git add -A` | Tüm yeni ve değiştirilmiş dosyaları git akışına/bekleme bölgesine ekle |
| `git commit -m "[notunuz]"` | Değişikliklere not bırak (opsiyonel değil *zorunludur.*) |
| `git rm -r [dosya-adi.txt]` | Bir dosya veya klasör sil |

### Branchlar(Dallanma) ve Merge(Birleştirme) işlemleri

| Komut | Açıklama |
| ----- | -------- |
| `git branch` | Branchları listele (sol tarafında yıldız işareti olan seçili branch'ı gösterir) |
| `git branch -a` | Bütün branchları listele (lokal ve uzak sunucudakileri de gösterir.) |
| `git branch [branch-adi]` | Yeni bir branch oluştur. |
| `git branch -d [branch-adi]` | Halihazırda oluşturulmuş olan bir branch'ı sil |
| `git push origin --delete [branch-adi]` | Uzak sunucudaki bir branch'ı sil |
| `git checkout -b [branch-adi]` | Yeni bir branch oluştur ve o branch'ı seç |
| `git checkout -b [branch-adi] origin/[branch-adi]` | Uzak sunucudaki projeyi lokal'e kopyala ve belirtilen branch'ı seç |
| `git checkout [branch-adi]` | Belirtilen branch'ı seç |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [dosya-adi.txt]` | Discard changes to a file |
| `git merge [branch-adi]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch-adi]` | Push a branch to your remote repository |
| `git push -u origin [branch-adi]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch-adi]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch-adi]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[kullaniciadi]/[proje-adi].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[kullaniciadi]/[proje-adi].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git diff [source branch] [target branch]` | Preview changes before merging |

