# Homework Ⅰ of The Fundamental Practice of Software Engineering Innovation

<div align="right" >
-----  QIchao Yuan 516051910027
</div>

# Vue.js

![vue logo](https://cn.vuejs.org/images/logo.png)





## 1. Overview

Vue.js is a **JavaScript front-end framework** that was built to organize and simplify **web** development.

The project focuses on making ideas in web UI development (components, declarative UI, hot-reloading, time-travel debugging, etc.) more approachable. It attempts to be less opinionated and thus easier for developers to pick up.

It features an incrementally adoptable architecture. The core library focuses on declarative rendering and component composition and can be embedded into existing pages. Advanced features required for complex applications such as routing, state management and build tooling are offered via officially maintained supporting libraries and packages.



## 2. Features

#### 1) Templates

 Using an HTML-based template syntax that allows you to declaratively bind the rendered DOM to the underlying Vue instance’s data.

#### 2) Reactivity

One of Vue’s most distinctive features is the unobtrusive reactivity system.

#### 3) Components

Components are one of the most powerful features of Vue. In a large application, it is necessary to divide the whole app into small, self-contained, and often reusable components to make development manageable. 

```javascript
<div id="tuto">
	<buttonclicked v-bind:initial_count="0"></buttonclicked>
</div>
<script>
Vue.component('buttonclicked', {
  props: ["initial_count"],
  data: function() {return {"count": 0} } ,
  template: '<button v-on:click="onclick">Clicked {{ count }} times</button>',
  methods: {
    "onclick": function() {
        this.count = this.count + 1;
    }
  },
  mounted: function() {
    this.count = this.initial_count;
  }
});

new Vue({
  el: '#tuto',
});
</script>
```

#### 4) Transitions

Vue provides a variety of ways to apply transition effects when items are inserted, updated, or removed from the DOM. This includes tools to:

- [ ] automatically apply classes for CSS transitions and animations
- [ ] integrate third-party CSS animation libraries, such as Animate.css
- [ ] use JavaScript to directly manipulate the DOM during transition hooks
- [ ] integrate third-party JavaScript animation libraries, such as Velocity.js

#### 5) Routing

In a single-page application (SPA) one initial disadvantage was the inability to share links to the exact "sub" page within a specific web page. Because SPAs serve their users only one URL-based response from the server (it typically serves index.html or index.vue), saving bookmarks, or sharing links to a specific article would be impossible. 

```javascript
<div id="app">
  <router-view></router-view>
</div>
const User = {
  template: '<div>User {{ $route.params.id }}</div>'
}

const router = new VueRouter({
  routes: [
    { path: '/user/:id', component: User }
  ]
})
```



## 3. Prons & Cons

#### Things for good：

> - It's so convenient to use the framework to support our projects.
> - Installing Vue and Vue Devtools is a little easier than installing vscode and configuring the environment for C++.
> - The procedures of running projects are obvious or visible for freshmen. 

#### Things for bad:

> - Things like Vue and React are somehow young so that there are many questions to be solved.
> - There is news saying that the front end work will be substituted by computer programs sooner or later.
> - Too many frameworks may confuse the new learners.

*Tips: Vue.js is so different with the technology stack I have had before, from the front end to the back end...*

~~To be honest, it feels so hard to learn it well.~~
