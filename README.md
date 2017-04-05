# PrintFirm Docker #

## Dependencies ##
[Docker](https://docker.github.io/engine/installation/)  
[PrintFirm.com Repo](https://bitbucket.org/printfirm/printfirm.com)  
[config.php file](https://bitbucket.org/snippets/printfirm/9ozAn)  
[git lfs](https://confluence.atlassian.com/bitbucket/use-git-lfs-with-bitbucket-828781636.html#UseGitLFSwithBitbucket-2.InstalltheGitLFSclientlocally)
  
  
## How do I get set up? ##

1. Clone this repo.
2. Clone the printfirm.com repo inside docker/ (a subfolder of this one) 
3. Switch printfirm.com repo to develop or a feature-branch
4. Use this [config.php file](https://bitbucket.org/snippets/printfirm/9ozAn). 
5. Edit hosts file(usually /etc/hosts) to have 127.0.0.1 also point to local.printfirm.com. If your hosts file isn't modified it should say, 127.0.0.1  locahost local.printfirm.com
6. Run `docker-compose build --pull && docker-compose up -d`
7. Move minimal DB to printfirm.com (must be named adminer.sql.gz)
8. Log into adminer with location/server 'mysql', user 'printfirm', and password 'password'.
10. Click on Import, then Run File in the "From Server" section.
9. Go into printfirm.com dir 
10. Run npm install
11. Run gulp less 

## How do I shut it down? ##

Run `docker-compose down`

## MySQL Info ##
```
#!yml

MYSQL_ROOT_PASSWORD: secret
MYSQL_DATABASE: printfirm
MYSQL_USER: printfirm 
MYSQL_PASSWORD: password
```