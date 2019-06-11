# vue.js
# vue.config 是一个对象，包含vue全局配置。vue.config.silent = true用来取消所有日志和警告
# vue.config.optionMergeStartegies自定义合并策略的选项
合并策略分别接收在父实例和子实例上定义的该选项的值作为第一个和第二个参数，vue实例上下文被作为第三个参数传入
#vue.extend使用基础vue构造器，创建一个‘子类’，参数是一个包含数组选项的对象
data选项是特例，需要注意-它在vue.extend中必须是函数
<div></div>
var Profile = Vue.extend({
  template: '<p>{{}}</p>',
  data: function () {
  return {
firstName:'11',
lastName:'22',
alias: '33'
}
  }
})
// 创建Profile实例，并且挂载到一个元素上去
new Profile().$mount('#mount-point')
# vue.nextTick
在下次dom更新循环结束之后延迟回调，在修改数据之后立即使用这个方法，获取更新后的dom
// 
vm.msg = 'Hello'
// dom还没更新
vue.nextTick(function(){
// dom更新了
})
# vue.set
向响应式对象中添加一个属性，并确保这个新的属性是响应式的，且触发视图更新，它必须用于向
响应式对象上添加新属性，
# vue.delete
删除对象的属性。如果对象是响应式的，确保删除能触发更新视图。这个方法主要用于避开vue不能检测到属性被删除的限制
