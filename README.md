# bash_bug_fix

This is a util tools to test if the centos/redhat 6/7 host has a bash bug

## how to use it

### 1. 测试是否有bug

执行：
./test_exist_bash_bug.sh

如果显示，则存在bug，需要进行安全升级：
vulnerable, sorry your host has bash bug
this is a test

如果显示，则不存在bug：
bash: warning: x: ignoring function definition attempt
bash: error importing function definition for `x'
this is a test


### 2. 根据不同的发行版，安装安全补丁升级包

redhat6/centos6:
 
 rpm -Uvh ./centos_redhat_6/*.rpm
 
 redhat7/centos7:
 
 rpm -Uvh ./centos_redhat_7/*.rpm

### 3. 再次测试

执行：
./test_exist_bash_bug.sh

如果显示，则存在bug，请联系我们：
vulnerable, sorry your host has bash bug
this is a test

如果显示，则不存在bug，恭喜：
bash: warning: x: ignoring function definition attempt
bash: error importing function definition for `x'
this is a test
