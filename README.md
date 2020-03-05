# vue-学习记录
vue学习记录
一、组件
  -- 组件传值问题 
    props: {
      xxx: String/Number/Boolean...,
      xxx: [String, Number, Boolean...],
      xxx: {
        type:String/Number/Boolean...,
        // 默认值
        default: xxx
      },
      // 带有默认值的对象
      xxx: {
        type: Object,
        // 对象或数组默认值必须从一个工厂函数获取
        default: function () {
          return { xxx: 'xxx' }
        }
      },
      // 自定义验证函数
      xxx: {
        validator: function (value) {
          // 这个值必须匹配下列字符串中的一个
          return ['success', 'warning', 'danger'].indexOf(value) !== -1
        }
      }
    }
  -- 导入组件及声明
  ∆ 导入：improtant xx from './xxx/xxx'
  ∆ 全局组件：Vue.component(xxx)
    局部组件：components{
                xxx,
                xxx: xxx,
                'xxx': xxx
             }
    使用：<xxx :xxx='xxx' />
