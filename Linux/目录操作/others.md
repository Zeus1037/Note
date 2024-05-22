### pwd

打印当前路径



### mkdir

创建文件夹



### nvidia-smi

查看显卡运行状态



### du -h --max-depth=1

### du -sh \* | sort -n

统计当前目录下所有文件夹大小，并按升序排序



### df -h

### du -sh # 查看当前目录大小总和





### ls -l | grep "^-" | wc -l

统计当前目录下文件的个数（不包括目录）

### ls -lR| grep "^-" | wc -l

统计当前目录下文件的个数（包括子目录）

### ls -lR | grep "^d" | wc -l

查看某目录下文件夹(目录)的个数（包括子目录）

### ls -l |grep -c "^d"

统计当前目录下文件夹个数



### find . -type d | sed -n '2,$p' | xargs rm -rf

删除当前目录下的所有文件夹，但不删除文件

### find -name "*.py"

找到当前目录下所有后缀为.py的文件



### rm -rf 

删除文件



### unzip

解压.zip压缩包

-d <dir> 解压到<dir>路径下