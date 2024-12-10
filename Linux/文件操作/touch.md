## touch

```shell
touch [options] <file>	# 若文件不存在，则创建<file>文件；否则修改<file>文件的时间戳属性为当前系统时间
```



#### options

   ```shell
   -a	# 仅改变<file>文件的Access时间记录
   -c	# 不创建新文件
   -m	# 仅改变<file>文件的Modify时间记录
   -r	<ref_file>	# 将<file>文件的时间戳属性修改为<ref_file>的时间戳
    
   --no-create	# 不创建新文件
   ```




#### Examples

-   ```shell
    touch 1.txt 2.txt 3.txt		# 同时创建多个文件
    ```

-   ```shell
    touch file.txt -r ref_file.txt	# 将file.txt文件的时间戳修改为ref_file.txt文件的时间戳
    ```
