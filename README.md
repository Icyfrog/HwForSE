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



