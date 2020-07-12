Git Komutları
============

## Dil Seçimi
- [English version (original)](README.md)
- [Versão em português](READMEpt.md)
___

_Sık sık kullanılan Git komutlarının listesi_

*Eğer git aliases ile ilgileniyorsanız, buradaki `.bash_profile`e bir göz atın: https://github.com/joshnh/bash_profile/blob/master/.bash_profile*

--

### Proje oluşturmak veya çağırmak

| Komut   | Açıklama    |
| ------- | ----------- |
| `git init` | Lokalde bir git deposu başlat (bulunduğunuz dosya dizinine git'i dahil eder) |
| `git clone ssh://git@github.com/[kullaniciadi]/[proje-adi].git` | Uzak sunucudaki projeyi lokalinize çağırır. |

### Basit Snapshot Komutları

| Komut   | Açıklama    |
| ------- | ----------- |
| `git status` | Durumu kontrol et |
| `git add [dosya-adi.txt]` | Git dizinine belirtilen dosyayı ekler |
| `git add -A` | Git dizinine bütün dosyaları ekler |
| `git commit -m "[aciklamaniz]"` | Değişiklikler hakkında bir açıklama veya kısa not belirtirsiniz. |
| `git rm -r [dosya-adi.txt]` | Git dizininden belirtilen dosyayı siler (veya klasörü) |

_Şu anlık burada kaldım, devam ediyor olacağım_

### Branch ve Merge
| Komut   | Açıklama    |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | Değişiklikleri göster |
| `git log --summary` | Değişiklikleri detaylı bir şekilde göster |
| `git diff [source branch] [target branch]` | Merge etmeden önce değişiklikleri göster |

