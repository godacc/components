
/**
* hash路由回退监控
* 基于hash 的路由 第一次会存储两条路由 回退就会回退两次 这里进行监听处理
*/
monitorRouterBack(){
window.onhashchange = function(event){
console.log('onhashchange',event.oldURL, event.newURL);
let newUrl = event.newURL;
let target = "/#/";
if(newUrl.lastIndexOf(target)==newUrl.length-target.length){
history.go(-2)
}
}
},