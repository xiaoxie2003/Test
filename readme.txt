2.  Git与SVN,CVS等的对比. 
     分布式vs集中式

3. 版本库? 目录, 被git管理, 此文件中文件的更新，删除，修改，git能跟踪,可以利用这个信息还原到历史的某一时刻. 
     git init    托管此目录

     .git   更新日志. 
4. git记录文本文件的更新.     plain text   
    图片，视频不行.  
    word不行, 为什么?   rich text

5. 向仓库中添加内容
    git add 文件名  
    git add .                                          添加本目录所有的文件
6. 提交. 
    git commit -m "第一次提交"
7. 如何查看仓库的状态. 
   git status
8. 如果通过git status查看文件有更新后，如何看出到底不同是在哪里呢?
   git diff 文件名
9. 查看提交历史, 显示从最近到最远的提交日志
   git log
10. 有了提交历史后，就可以进行回退操作了. 
      回到以前    git reset --hard HEAD^
                       git reset --hard  commitid
11. 认知 git 仓库结构. 
     工作区 -> 暂存区  -> 提交区
12. 
  如暂存区没有，而工作目录更新，要撤销这些更新: git restore 文件名
  如工作区的内容已经add到暂存区，且工作区又更新过，要丢弃工作区修改. 
           git checkout -- 文件名
  如已经commit到提交区，要将暂存区的更新部分撤销 
          git reset HEAD 文件名

   这两个操作加起来就是   git reset --hard xxx的操作了. 

   
13. 从github clone仓库
    git clone   xxxx地址
14. 提交本地仓库中已经commit的数据到github
   git push origin main