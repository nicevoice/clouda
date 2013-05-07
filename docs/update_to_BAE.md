# Framework托管到BAE


Framework是基于node.js开发的，所以需要node.js环境以及需要数据库的支持，百度开发者中心上BAE提供整套的环境的支持，只需简单的配置就可以快速运行基于framework开发的应用，具体方法如下：







![](images/intro_4_4.png)

![](images/intro_4_5.png)

（6）“创建新版本”，并使用SVN下载版本代码

![](images/intro_4_6.png)

（7）将本地sumeru工程文件拷贝到SVN下载版本代码目录下

  		- url : ^/socket/(.*)
    		script: $1.nodejs

  		- url : ^/view/(.*)
    		script: /__bae__/bin/view/$1

  		- url : ^/bin/(.*)
    		script: /__bae__/bin/$1

  		- url : ^/hiUpload/(.*)
    		script: /__bae__/static/hiUpload/$1

  		- url : /server/(.*)
    		script: /index.html

  		- url : ^/publish/(.*)
    		script: /index.html

  		- url : (*.ico)
    		script: $1
  
  		- url : ^/sumeru/(.*)
    		script : /sumeru/$1
  
  		- url : ^/sumeru\.js
    		script : /sumeru/sumeru.js
    
  		- url : (.*)
    		script: /app/$1
    
  		- expire : .* modify 0 seconds
  		- expire : .jpg modify 10 years
  		- expire : .swf modify 10 years
  		- expire : .png modify 10 years
  		- expire : .gif modify 10 years
  		- expire : .JPG modify 10 years
  		- expire : .ico modify 10 years
  
  		- mime: .manifest text/cache-manifest
  		
  		
  也可点击<http://pan.baidu.com/share/link?shareid=474214&uk=1077217927>下载该文件






    password = " ";



    	"main": "app.js"
	}

（15）访问您自己的应用地址，如果您是使用示例程序，可以访问 域名+index.html#/itworks