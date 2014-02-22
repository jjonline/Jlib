Jlib
====
Jlib,JJonline javascript libaray

/**
+----------------------------------------------------------
* 
* @authors: Jea Yang (JJonline@JJonline.Cn)
* @CopyRights: Any source code changes without permission prohibited
* @Time: 2014-02-12 13:45:16
* @Time: 2014-02-19 Add J.cookie() &&  J.localData()
* @Time: 2014-02-22 fix <=ie7 object of JSON , Merge JSON2.js to Jlib.js && Add  J.toString() &&  J.toObject() && J.isCardNumber()[同名函数J.isID()]
* @Description: Jlib.js === jjonline javascript libaray
* @version 1.1.1 dev
*
*@ Api
* 产生随机整数方法  =>  J.rand([min],[max]); 
* 产生随机字符串[去除易混淆的0、1、I、l、L、O、o] => J.randString([length])
* 去除字符串中所有空白 => J.trimAll(str);
* 检测传入的字符串是否是邮箱格式 => J.isMail(str)
* 检测传入的字符、数字字符串是否是手机格式 =>J.isPhone(num)
* 检测传入的字符串是否是中文 => J.isChinese(str)
* 检测传入的字符串是否是正整数 => J.isNumber(num)
* 检测传入的字符串是否是QQ号码 => J.isQQ(qq)
* 检测传入的字符串是否是合法网址 => J.isUrl(url)
* 检测传入的字符串是否是合法密码格式 => J.isPassWord(pwd)
* 检测传入的字符串是否是全部由字母构成 => J.isAlphabet(Alphabets)
* 检测传入的字符串是否是合法的天朝身份证号码[严格效验] => J.isID(CardNumber) 或 J.isCardNumber(CardNumber)
* 传入当前页面的url中的get变量名称获取当前url中的get变量 => J.GetUrlQueryString(getName)
* 获取当前窗口的宽高,返回对象 => J.windowSize()
*
*
* cookie操纵函数方法，类似jquery.cookie => J.cookie(key,[value],[{expires: 365, path: '/', domain: 'jjonline.cn',secure: false}]) 
* ====> 读取cookie  => J.cookie(CookieName) 或 J.Cookie(CookieName);
* ====> 删除cookie  => J.cookie(CookieName,null) 或 J.cookie(CookieName,'null') 或 J.Cookie(CookieName,null) 或 J.Cookie(CookieName,'null')
* ====> 设置cookie  => J.cookie(CookieName,CookieValue,options)  或 J.Cookie(CookieName,CookieValue,options)
* ========> 设置cookie时options参数为json对象格式 格式范例 => {expires: 365, path: '/', domain: 'jjonline.cn',secure: false}
* ========> J.cookie方法中options参数说明 => expires为过期时间，单位：天，可以设置该参数为负数达到删除cookie的效果；
* ========> path为cookie作用目录，默认'/'，整站可用；
* ========> domain为cookie的作用域，默认当前域名下；
* ========> secure为是否该cookie仅作用于安全链接，默认所有链接可用
*
*
* 本地相对永久存储文本数据[<=ie7使用userData，建议文本大小不要大于64K、其他使用localStorage] =>J.localData(key,[value])
* ====> 读取本地数据  => J.localData(key)
* ====> 删除本地数据  => J.localData(key,null) 或 J.localData(key,'null')
* ====> 设置本地数据  => J.localData(key,value)
* ====> 清空本地数据  => J.localData('null') 或 J.localData(null)
* PS：该方法目前默认仅接受value参数为字符串类型的文本，若要存储其他类型数据请使用J.toString()方法转换成字符串后存储，取出后使用J.toObject()还原即可
*
*
* 将对象[object of json 、object of array]转换成字符串方法 => J.toString(object)
* 将对象字符串[需符合对象字符串的格式要求]转换成对象方法 => J.toObject(objectString)
* PS：目前Jlib.js已经将开源的JSON2.js合并，所有浏览器中可直接调用JSON.parse()、JSON.stringify()等JSON原生方法
+----------------------------------------------------------
*/

