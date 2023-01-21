<script>
  import { Meteor } from 'meteor/meteor';
  import Router from 'svelte-spa-router';
  import { wrap } from 'svelte-spa-router/wrap'
  import LayoutStatic from './pages/LayoutStatic.svelte';
  import LayoutSideNavLight from './pages/LayoutSideNavLight.svelte';
  import Unauthorized from './pages/_401.svelte';
  import FileNotFound from './pages/_404.svelte';
  import ServerError from './pages/_500.svelte';
  import Login from './pages/Login.svelte';
  import PasswordRecovery from './pages/PasswordRecovery.svelte';
  import Register from './pages/Register.svelte';
  import Home from './pages/demo/Home.svelte';
  import Charts from './pages/demo/Charts.svelte';
  import Tables from './pages/demo/Tables.svelte';

  let target = 'page';
  $m: {
      routes = {
        '/': Home,
        '/charts': Charts,
        '/tables': Tables,
        "/layout-static": LayoutStatic,
        "/layout-sidenav-light": LayoutSideNavLight,
        "/login": Login,
        "/password-recovery": PasswordRecovery,
        "/register": Register,
        "/500": ServerError,
        "/401": Unauthorized,
        "*": FileNotFound
    };
  }
</script>

<Router {routes}/>