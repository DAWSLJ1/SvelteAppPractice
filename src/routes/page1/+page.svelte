<script>
import bill from ''
import Header from "../lib/assets/components/Header.svelte";
import Footer from "../lib/assets/components/Header.svelte";

let firstName = "Hello";
let lastName = $state("World");
let fullName = $derived(firstName + " " + lastName)

firstName = "Web";
lastName = "two";
</script>

<Header>
    <h2>About Us</h2>
    <p>This is the about page</p>

    <p>First : {firstName}</p>
    <p>Last : {lastName}</p>
    {#if firstName && lastName}
    <p>Hi, {fullName}</p>
    {/if}
    
</Header>

<main>
<nav>
        <ul>
           <li><a href="/blog/first">FirstBlog</a></li>
           <li><a href="/blog/apple">Apple</a></li>
           <li><a href="/blog/next">Next</a></li>
           <li><a href="/blog">Blog</a></li>
        </ul>
      </nav>
</main>

<Footer />
<style>


</style>
