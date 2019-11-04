私有仓库源，配置方法：

开一个repo，这个repo就是我们私有Pod源仓库，也就是当前的repo

pod repo add [私有Pod源仓库名字] [私有Pod源的repo地址]
也就是pod repo add [当前项目的名字] [当前项目的repo地址]

项目最终打包收尾工作，

1）直接在每个项目的目录中都使用./upload.sh脚本进行上传

2）或者使用以下命令
git add .
git commit -m "版本号"
git tag 版本号
git push origin master --tags
./upload.sh
