## mkdir	<!--make directory-->

```shell
mkdir [options] <dir>	# 在当前目录下创建<dir>目录
```



#### options

```shell
-p			# 递归创建目录
-m <xxx>	# 创建目录时设置文件权限为<xxx>
-v			# 显示目录的创建过程
```



#### examples

-   ```shell
    mkdir dir1 dir2 dir3		# 在当前目录下同时创建dir1、dir2、dir3目录
    ```

-   ```shell
    mkdir -p dir1/dir2/dir3		# 在当前目录下递归创建dir1/dir2/dir3目录
    ```
