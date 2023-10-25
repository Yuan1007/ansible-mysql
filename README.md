----------
### git 操作指令

#### 設定遠端倉庫
1. 新增遠端倉庫
` git remote add origin https://github.com/username/repository.git `
ex: git remote add origin https://github.com/Yuan1007/ansible-mysql.git
origin: 一個名為 origin 的遠端倉庫，可以將origin看作是別名
2. 修改遠端倉庫
` git remote set-url origin https://github.com/username/repository.git `
3. 驗證遠端倉庫
` git remote -v `
4. 推送至遠端倉庫
git push
ex:  ` git push -u origin main `
5. 刪除設定的遠端倉庫
` git remote remove ${指定的遠端倉庫名稱} `
6. git 分支重新命名
` git branch -m development `
7. 檢查git目前使用的帳戶跟mail
` git config user.name ` 
` git config user.email ` 
8. 複製公鑰指令
` cat ~/.ssh/id_rsa.pub | pbcopy ` # MacOS
` cat ~/.ssh/id_rsa.pub | xclip -selection clipboard ` # Linux

----------
### 操作指南
1. 在 inventory的hosts檔案 設定要安裝的mysql版本
    mysql_version="5.7" or mysql_version="8"

2. 驗證 MySQL 容器是否運行
` docker ps | grep mysql `

3. 連線docker 容器
` docker exec -it 053a4a633975 /bin/bash `
 **053a4a633975** => 這邊請改為你的container id

4. 使用 mysql 工具來連接到 MySQL
` mysql -u root -p `
預設: root/123456

5. 創建一個新的 MySQL 使用者：
` CREATE USER 'newuser'@'%' IDENTIFIED BY 'password'; `

6. 給予給這個新使用者完全的權限
` GRANT ALL PRIVILEGES ON *.* TO 'newuser'@'%' WITH GRANT OPTION; `

7. 刷新權限生效
` FLUSH PRIVILEGES; `

8. 測試連接
` mysql -u newuser -p `

9. 修改root密碼
` ALTER USER 'root'@'localhost' IDENTIFIED BY 'new_password'; `

10. 刷新權限生效
` FLUSH PRIVILEGES; `

11. phpmyadmin 登入資訊
mysql/root/123456
