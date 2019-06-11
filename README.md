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
