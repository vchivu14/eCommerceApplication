<script>
    import { SvelteToast } from "@zerodevx/svelte-toast";
    import { Router, Route, Link } from "svelte-routing";
    import ProtectedRoute from "./routes/ProtectedRoute.svelte";
    import Home from "./pages/Home.svelte";
    import Profile from "./pages/Profile.svelte";
    import Login from "./pages/Login.svelte";
    import Signup from "./pages/Signup.svelte";
    import ForgotPassword from "./pages/ForgotPassword.svelte";
</script>

<SvelteToast/>
<!-- Router: This component is used for providing extra routing information to every Link and Route components inside it. 
    Because of this, you need at least one top-level Router in your application -->
<!-- Route: This component specifies a route. It expects a path property that defines when your component 
    — that is passed to component — should be rendered. -->
<!-- ProtectedRoute component that we will use to protect pages from unauthorized access. -->
<Router>
    <Route path="/" component={Home}/>
    <Route path="/login" component={Login}/>
    <Route path="/register" component={Signup}/>
    <Route path="/forgot-password" component={ForgotPassword}/>
    <ProtectedRoute path="/profile" component={Profile}/>
</Router>