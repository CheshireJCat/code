## 表单
<div class="codes">
<div class="form">
<div class="input-field s50">
    <input class="inputText" id="first_name" type="text">
    <label for="first_name">First Name</label>
</div>
<div class="input-field s50 fr">
    <input class="inputText" id="last_name" type="text">
    <label for="last_name">Last Name</label>
</div>
<div class="input-field s100">
  <input class="inputText" disabled value="I am not editable" id="disabled" type="text">
  <label for="disabled">Disabled</label>
</div>
</div>
<div class="input-field s100">
  <input class="inputText" id="password" type="password">
  <label for="password">Password</label>
</div>
<div class="input-field s100">
  <input class="inputText" id="email" type="email">
  <label for="email">Email</label>
</div>
<div class="input-field textarea s100">
  <textarea class="inputText" id="textarea1"></textarea>
  <label for="email">Textarea</label>
</div>
</div>
<style type="text/css">
	.form{width: 100%;}
	.input-field{position: relative;margin-top: 15px;}
	.s50{width: 45%;padding:0 15px;margin-left: -15px;float: left;}
	.fl{float: left;}
	.fr{float: right;}
	.s100{width: 100%;float: left;}
	.inputText{
		background-color: transparent;border: none;border-bottom: 1px solid #9e9e9e;border-radius: 0;outline: none;
		height: 35px;width: 100%;font-size: 15px;line-height: 35px;margin: 0 0 15px 0;padding: 0;box-shadow: none;box-sizing: content-box;
		transition: all .3s;
	}
	textarea.inputText{overflow-y: auto;resize:none;min-height:70px;height:auto;border:1px solid #9e9e9e;}
	.input-field label{color: #9e9e9e;position: absolute;font-size: 1rem;font-size: 15px;cursor: text;transition: .2s ease-out;top:14px;}
	.input-field label.active{transform: translateY(-140%);font-size: 12px;top:0px;}
	.inputText:focus:not([readonly]) {border-color: #26a69a;box-shadow: 0 1px 0 0 #26a69a;}
</style>
<script type="text/javascript">
	$(".inputText").each(function(){
		if($(this).val()||$(this).attr("Placeholder")){
			$(this).siblings('label').addClass('active');
		}
	});
		$(".inputText")
	.focusin(function(){$(this).siblings('label').addClass('active');})
	.focusout(function(){
		if(!$(this).val()){
			if(!$(this).attr("Placeholder")){
				$(this).siblings('label').removeClass('active');
			}else{
				$(this).siblings('label').addClass('active');
			}
		}else{
			$(this).siblings('label').addClass('active');
			
		}
	});
</script>
</div>
##### html
```
<div class="form">
    <div class="input-field s50">
        <input class="inputText" id="first_name" type="text">
        <label for="first_name">First Name</label>
    </div>
    <div class="input-field s50 fr">
        <input class="inputText" id="last_name" type="text">
        <label for="last_name">Last Name</label>
    </div>
    <div class="input-field s100">
      <input class="inputText" disabled value="I am not editable" id="disabled" type="text">
      <label for="disabled">Disabled</label>
    </div>
    </div>
    <div class="input-field s100">
      <input class="inputText" id="password" type="password">
      <label for="password">Password</label>
    </div>
    <div class="input-field s100">
      <input class="inputText" id="email" type="email">
      <label for="email">Email</label>
    </div>
    <div class="input-field textarea s100">
      <textarea class="inputText" id="textarea1"></textarea>
      <label for="email">Textarea</label>
    </div>
</div>
```
##### style
```
<style type="text/css">
	.form{width: 100%;}
	.input-field{position: relative;margin-top: 15px;}
	.s50{width: 45%;padding:0 15px;margin-left: -15px;float: left;}
	.fl{float: left;}
	.fr{float: right;}
	.s100{width: 100%;float: left;}
	.inputText{
		background-color: transparent;border: none;border-bottom: 1px solid #9e9e9e;border-radius: 0;outline: none;
		height: 35px;width: 100%;font-size: 15px;line-height: 35px;margin: 0 0 15px 0;padding: 0;box-shadow: none;box-sizing: content-box;
		transition: all .3s;
	}
	textarea.inputText{overflow-y: auto;resize:none;min-height:70px;height:auto;border:1px solid #9e9e9e;}
	.input-field label{color: #9e9e9e;position: absolute;font-size: 1rem;font-size: 15px;cursor: text;transition: .2s ease-out;top:14px;}
	.input-field label.active{transform: translateY(-140%);font-size: 12px;top:0px;}
	.inputText:focus:not([readonly]) {border-color: #26a69a;box-shadow: 0 1px 0 0 #26a69a;}
</style>
```
##### javascript
```
<script type="text/javascript">
	$(".inputText").each(function(){
		if($(this).val()||$(this).attr("Placeholder")){
			$(this).siblings('label').addClass('active');
		}
	});
		$(".inputText")
	.focusin(function(){$(this).siblings('label').addClass('active');})
	.focusout(function(){
		if(!$(this).val()){
			if(!$(this).attr("Placeholder")){
				$(this).siblings('label').removeClass('active');
			}else{
				$(this).siblings('label').addClass('active');
			}
		}else{
			$(this).siblings('label').addClass('active');
			
		}
	});
</script>
```