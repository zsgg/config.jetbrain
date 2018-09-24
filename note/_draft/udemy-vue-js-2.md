![alt book](https://udemy-images.udemy.com/course/240x135/995016_ebf4.jpg)

###[api document](https://vuejs.org/v2/api)
###section2 : using VueJs to interaction with DOM
####vue instance 에서의 this
- 안되는 곳에선 `var vm = this`;
```
new Vue({  
    el: '#app',  
    data: {  
        title: 'Hello World!'  
    },  
    methods: {  
        changeTitle: function (event) {  
            //여기의 this는 function의 this 이지만 vue js 에서 function안의 this는 vue instatnce도 포함한다  
            this.title = event.target.value;  
        }  
    }  
});  
```

####[methods vs computed](https://kr.vuejs.org/v2/guide/computed.html)


####css class bind
- `:style`도 유사
	- `backgroundColor: this.color`

```
//1
    :class="{red: isRed}"
//2
    computed:{
        divClasses: function(){
            return {
                red: this.att,
                blue: !this.att
            }
        }
    }
//3
    v-model
```


####Useful Links
#####[Getting Started](https://jsfiddle.net/smax/pcjtcmdm/)
#####[Template Syntax](https://jsfiddle.net/smax/bkk97b7g/)
#####[Events](https://jsfiddle.net/smax/7zdak05g/)
#####[Two-Way-Binding](https://jsfiddle.net/smax/ut0tsbcu/)
#####[Computed Properties & Watch](https://jsfiddle.net/smax/yLjqxmw0/)
#####[Dynamic Classes](https://jsfiddle.net/smax/gowg40ym/)
#####[Dynamic Styles](https://jsfiddle.net/smax/3rvdLq5y/)


###Section3 : Using Condiftionals and Rendering Lists
####object v-for
```
<div v-for="(value, key, index) in person"></div>
```
####array v-for
```
<div v-for="(person, index) in persons"></div>
```
####number v-for
```
<div v-for"n in 10"></div>
```

####Useful Links
#####[Conditionals (v-if and v-show)](https://jsfiddle.net/smax/hoc719j5/)
#####[Lists](https://jsfiddle.net/smax/o7uy2g0u/)



###Section5 : Understanding the VueJs Instance
####Useful Links
#####[The Vue Instance Code](https://jsfiddle.net/smax/9a2k6cja/2/)
#####[The VueJS Instance Lifecycle](https://jsfiddle.net/smax/jcgw7ak8/)


###Section7 : An Introduction to Components









