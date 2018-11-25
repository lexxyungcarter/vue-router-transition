# vue-router-transition
A vue 2 awesome vue-router page transitions for your application

## Install
`npm install vue-router-transition`

## Options (Props)

### transition
- fade (default)
- slide
- sliding

### mode
- out-in (default)
- in-out

e.t.c.

# Usage
## Method 1
* In your code, just below the `<router-link></router-link>` just import it like so : `import TransitionPage from 'vue-router-transition';`

```js
<transition-page transition="slide">
    <router-view></router-view>
</transition-page>
```

* You can also add it to your component as components. If you want it globally available
you can just to this : `Vue.component('transition-page', TransitionPage);`
* Check the [examples](#examples) on how to use it in your template

# Examples
Using the default options, you just need to pass an id and a model
```
<transition-page transition="sliding" mode="in-out">
    <router-view></router-view>
</transition-page>
```

Laravel/Blade/Vue.js
```php
// sidebar.blade.php

@php
    $route = $navigation['route'];
    $route = isset($navigation['default']) ? route($route, [$navigation['default']]) : route($route);
@endphp

<router-link to="{{ relativeUrl($route) }}" tag="v-list-tile">
    <v-list-tile-content title="{{ relativeUrl($route) }}">
        <v-list-tile-title >
            {{ $link['name'] }}
        </v-list-tile-title>
    </v-list-tile-content>
</router-link>
```

```php
// main.blade.php

@include('layouts.partials.sidebar')

<transition-page transition="slide">
    <router-view></router-view>
</transition-page>
```

## Contribution
The package has been kept as simple as possible to offer a starting point for your next project. We are looking for more
css page transitions and we would be more than grateful to receive your pull-requests. You can also share a gist containing
the css transition for us to add.

Cheers!

## Credits
- [Lexx YungCarter](https://github.com/lexxyungcarter)
- [maoberlehner](https://github.com/maoberlehner/vue-router-page-transitions)