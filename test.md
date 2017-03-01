
服务器测试

2017-03-01 22:06:39,113 INFO Tom login success
2017-03-01 22:06:46,965 INFO John login success
2017-03-01 22:06:52,933 INFO Lucy login success
2017-03-01 22:07:04,024 INFO Lucy transfer file 1.md done
2017-03-01 22:07:04,025 INFO Lucy push file 1.md success
2017-03-01 22:07:04,028 INFO Lucy disk space info fresh success
2017-03-01 22:07:32,000 WARNING Lucy of disk space is not enough
2017-03-01 22:09:57,835 INFO Lucy start to transfer 123.wma
2017-03-01 22:09:58,601 INFO Lucy has finished to transfer 123.wma
2017-03-01 22:10:36,443 INFO Lucy quit
2017-03-01 22:10:53,328 INFO John quit
2017-03-01 22:11:02,553 WARNING client disconnect

-----------------------------------------------------------------------------------------------------

客户端测试

Enter username: Lucy
Enter password: 123
	 welcome Lucy
[Lucy@Lucy]$ push 1.md
2017-03-01 22:07:04,029 INFO upload file: 1.md success
[Lucy@Lucy]$ push 123.wma
2017-03-01 22:07:32,000 WARNING disk space is not enough
[Lucy@Lucy]$ push dd dd
2017-03-01 22:07:40,653 WARNING need 2 parameters, but give 3 parameters
[Lucy@Lucy]$ pssj
	请输入help，进行查询
[Lucy@Lucy]$ help
请输入以下命令：

        ls
        pwd
        cd ..
        cd dirname
        push filename
        pull filename
        
[Lucy@Lucy]$ cd ..
2017-03-01 22:08:00,553 WARNING You must change directory in home directory
[Lucy@Lucy]$ ls
----content list----
1.md
123.wma
--------------------
[Lucy@Lucy]$ pwd
/home/Lucy
[Lucy@Lucy]$ ls
----content list----
1.md
123.wma
test
--------------------
[Lucy@Lucy]$ cd 1.md
2017-03-01 22:09:08,306 WARNING Not a directory
[Lucy@Lucy]$ cd haha
2017-03-01 22:09:14,931 WARNING No such file or directory
[Lucy@Lucy]$ cd test
[Lucy@test]$ pwd
/home/Lucy/test
[Lucy@test]$ cd ..
[Lucy@Lucy]$ ls
----content list----
1.md
123.wma
test
--------------------
[Lucy@Lucy]$ pull 123.wma
2017-03-01 22:09:57,836 INFO file 123.wma is receiving ...
2017-03-01 22:09:57,905 INFO recv ..... 10.02%
2017-03-01 22:09:57,970 INFO recv ..... 20.01%
2017-03-01 22:09:58,043 INFO recv ..... 30.02%
2017-03-01 22:09:58,120 INFO recv ..... 40.01%
2017-03-01 22:09:58,196 INFO recv ..... 50.02%
2017-03-01 22:09:58,276 INFO recv ..... 60.05%
2017-03-01 22:09:58,354 INFO recv ..... 70.01%
2017-03-01 22:09:58,438 INFO recv ..... 80.07%
2017-03-01 22:09:58,522 INFO recv ..... 90.04%
2017-03-01 22:09:58,601 INFO recv ..... 100.00%
2017-03-01 22:09:58,602 INFO file 123.wma has received done
2017-03-01 22:09:58,602 INFO file 123.wma has downloaded successfully
[Lucy@Lucy]$ quit

Process finished with exit code 0

