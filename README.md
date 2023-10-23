----------
git 操作指令

設定遠端倉庫

    1. 新增遠端倉庫
    ``` git remote add origin https://github.com/username/repository.git ```
    ex: git remote add origin https://github.com/Yuan1007/ansible-mysql.git
    origin: 一個名為 origin 的遠端倉庫，可以將origin看作是別名
    2. 修改遠端倉庫
    ``` git remote set-url origin https://github.com/username/repository.git ```
    3. 驗證遠端倉庫
    ``` git remote -v ```
    4. 推送至遠端倉庫
    ``` git push ```
    ex:  git push -u origin main
    5. 刪除設定的遠端倉庫
    ``` git remote remove ${指定的遠端倉庫名稱} ```
    6. git 分支重新命名
    ``` git branch -m development ```