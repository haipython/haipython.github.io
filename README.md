
<html>
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8"/>
    <title>登录页面</title>
    <link href="css/common.css" rel="stylesheet" />
    <link href="css/account.css" rel="stylesheet" />
</head>
<body>
	<div class='account-container mt30'>
        
        <div class='body clearfix pd10' style='position: relative;'>
        	<div class='logo left'>
        		<img style='height:3px;' src="images/login_logo.png" />
        	</div>
        	<div class='login left mt30'>
        		<form id='Form' action='/account/login' method='POST'>
	        		
	        		<div class='group mt10'>
	                	<label class='tip'><span class="red">*</span>用户名：</label>
	                	<input type='text' require='true' label='用户名' Field='string' range='4-40' name='username' />
	                	<i class='i-name'></i>
	                </div>
	              
	                <div class='group'>
	                	<label class='tip'><span class="red">*</span>密码：</label>
	                	<input  type='password' require='true'  label='密码' min-len='6' name='pwd' />
	                	<i class='i-pwd'></i>
	                </div>
	               
	                <div class='group'>
	                	<label class='tip'><span class="red">*</span>验证码：</label>
	                	<input  type='text' require='true' label='验证码' style='width:80px;' name='checkcode' />
	                    <a style='width:125px;display:inline-block;'><img class='checkcode' onclick='ChangeCode();' id='imgCode' src='/account/check' /></a>
	                </div>
	                <div class='group font12 mb0'>
	                	<label class='tip'></label>
	                	<label style='width:246px;display: inline-block;'>
	                        <input id='protocol' name='protocol' type='checkbox' checked='checked' />
	                        <span>自动登录</span>
	                        <span class='ml10'><a href='#'>忘记密码？</a></span>
	                    </label>
	                </div>
	                <div class='group mt0'>
	                	<label class='tip'></label>
	                	<input type='submit' class='submit' value='登	录' />
	                </div>
	        	</form>
	        	
	        	<div class='go-register'><a href='/account/register'>免费注册 >> </a></div>
        	</div>
        </div>
		
	</div>
	
	<div class='account-container mt20' style='text-align:center;color:#555;'>
		© 2004-2015 www.autohome.com.cn All Rights Reserved.  版权所有
	</div>
	
	
	<script src="js/jquery-1.8.2.min.js"></script>
	<script src="js/wupeiqi.js"></script>
    <script type="text/javascript">
    	
    	$(function(){
    		$.login('#Form','');
    	})
    
	    function ChangeCode() {
            var code = document.getElementById('imgCode');
            code.src += '?';
        }
    </script>
</body>
</html>
