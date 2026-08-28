<script lang="ts">
  import { goto } from "$app/navigation";
  import { type Locale } from "$lib/Locale";
  import Footer from "../../Footer.svelte";
  import Header from "../../Header.svelte";
  import type { PageData } from "./$types";

  let { data }: { data: PageData } = $props();
</script>

<Header locale={data.locale as Locale} />

<section>
  <div class="section-inner main relative">
    <div class="absolute top-4 right-4 flex flex-col items-end gap-2">
      <div class="top-4 right-4 flex gap-2">
        <button onclick={() => goto("/sign-in")}>Sign in</button>
        <button onclick={() => goto("/register")}>Register</button>
      </div>

      <button onclick={() => goto("/register")}>Settings</button>
    </div>
    <h1 class="pr-48 text-4xl mb-4">Welcome to the Remote Firmware Manager.</h1>
    <h2 class="pr-48 mb-6">
      Here you can manage software on real hardware devices in the lab.
      To start your journey, register or sign in (top right).
    </h2>
    <h2>
      Check out the source code of this website and the backend here: https://github.com/Hugos-Tech-Lab/Remote-Firmware-Manager
    </h2>

    <!-- <h1>Select Location</h1>
    <button>Hugo's Tech Lab</button>
    <h1>Select Device</h1>
    <button>Car1</button>
    <button>Car2</button>
    <h3>We support you with electronics, tools, and programming..</h3> -->
  </div>
</section>

<Footer />
