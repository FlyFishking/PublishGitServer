/********************** gitblit install **************************/
1、install java sdk and add envparams
    A、 add new JAVA_HOME  D:\Program Files (x86)\Java\jdk1.6.0_21 (your own installer path)
    B、 edit    PATH       %JAVA_HOME%/bin;%JAVA_HOME%/jre/bin
    C、 add new CLASSPATH  .;%JAVA_HOME%/lib/dt.jar;%JAVA_HOME%/lib/tools.jar
2、unzip gitblit-1.*.zip, download from: http://www.gitblit.com/
3、add git repository folder
/********************** gitblit config **************************/
1、Copy gitblit.properties file to gitblit-1.*/data folder
2、Run  gitblit-1.*/gitblit.cmd to check gitblit site run wheather right or not
   gitblit site is setting in the step.1, e.g.http://localhost:XXXX
3、Run installService.cmd to add to windowsservice and set it run automaticly
   Tips:
    A、Befor you run the installService.cmd file you should add some node like SET CD=C:\Git\gitblit-1.8.0 after SET ARCH=amd64
    B、Maybe you can  also change --StartParams="--storePassword;gitblit;--baseFolder;%CD%\data" ^ to be --StartParams="" ^
4、You can see git is added into the windows services and running auto

