<script lang="ts">
  import GridBackground from "#lib/components/GridBackground.svelte";

  const features = [
    {
      title: "Fast and lightweight",
      body: "Built with Svelte and Vite. Pages load quickly and the panel stays responsive, even with many servers running.",
    },
    {
      title: "Full control",
      body: "Manage servers, users, and settings in one place. Give each person exactly the access they need with fine-grained permissions.",
    },
    {
      title: "Made to be read",
      body: "A clean dark interface that keeps stats and actions easy to scan at a glance.",
    },
  ];

  const steps = [
    { title: "Deploy", body: "Pick a game and create a server in a few clicks." },
    { title: "Configure", body: "Set resources, startup options, and who can access it." },
    { title: "Monitor", body: "Keep an eye on your servers from one screen." },
  ];
</script>

<svelte:head>
  <title>Neoactyl: modern game server panel</title>
  <meta
    name="description"
    content="Neoactyl is a modern, lightweight panel for deploying, configuring, and monitoring game servers."
  />
</svelte:head>

<GridBackground />

<div class="relative z-10 min-h-screen text-slate-200 selection:bg-indigo-400/30">
  <!-- Header -->
  <header class="mx-auto flex max-w-6xl items-center justify-between px-6 py-6">
    <a href="/" class="focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-indigo-300">
      <img src="/logo.svg" alt="Neoactyl" width="120" class="block" />
    </a>
    <nav class="flex items-center gap-2 text-sm">
      <a href="#features" class="hidden px-3 py-2 text-slate-300 transition hover:text-white focus-visible:outline-2 focus-visible:outline-indigo-300 sm:block">Features</a>
      <a href="#how" class="hidden px-3 py-2 text-slate-300 transition hover:text-white focus-visible:outline-2 focus-visible:outline-indigo-300 sm:block">How it works</a>
      <a
        href="https://github.com/neoactyl"
        target="_blank"
        rel="noopener noreferrer"
        class="border border-white/10 bg-white/5 px-4 py-2 font-medium text-white transition hover:bg-white/10 focus-visible:outline-2 focus-visible:outline-indigo-300"
      >
        GitHub
      </a>
    </nav>
  </header>

  <main class="mx-auto max-w-6xl px-6">
    <!-- Hero -->
    <section class="pb-24 pt-14 lg:pb-32 lg:pt-24">
      <div class="max-w-3xl">
        <p class="mb-6 inline-flex items-center gap-2 border border-amber-300/30 bg-amber-300/10 px-3 py-1 text-sm text-amber-200">
          <span class="size-2 bg-amber-300 motion-safe:animate-pulse"></span>
          Under development
        </p>

        <h1 class="bg-gradient-to-br from-white to-indigo-200 bg-clip-text text-5xl font-extrabold leading-[1.05] tracking-tight text-transparent sm:text-6xl lg:text-7xl">
          Game server management, reimagined.
        </h1>

        <p class="mt-6 max-w-xl text-lg leading-relaxed text-slate-300">
          Neoactyl is a modern, lightweight panel for managing game servers. Deploy, configure, and monitor everything from a fast, clean interface.
        </p>

        <div class="mt-9 flex flex-col gap-3 sm:flex-row">
          <a
            href="https://neoactyl.app/"
            target="_blank"
            rel="noopener noreferrer"
            class="inline-flex items-center justify-center bg-white px-7 py-3.5 font-semibold text-slate-900 shadow-[0_10px_30px_-10px_rgba(255,255,255,0.4)] transition hover:-translate-y-0.5 hover:shadow-[0_14px_36px_-10px_rgba(255,255,255,0.5)] focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-300"
          >
            Get started
          </a>
          <a
            href="https://github.com/neoactyl"
            target="_blank"
            rel="noopener noreferrer"
            class="inline-flex items-center justify-center border border-white/10 bg-white/5 px-7 py-3.5 font-semibold text-white transition hover:bg-white/10 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-300"
          >
            View on GitHub
          </a>
        </div>
      </div>

    </section>

    <!-- Features -->
    <section id="features" class="scroll-mt-8 border-t border-white/10 py-24">
      <h2 class="max-w-2xl text-3xl font-bold tracking-tight text-white sm:text-4xl">
        Everything you need to run your servers.
      </h2>

      <div class="mt-12 grid gap-4 md:grid-cols-6">
        <div class="border border-white/10 bg-white/[0.03] p-8 md:col-span-4">
          <h3 class="text-xl font-semibold text-white">{features[0].title}</h3>
          <p class="mt-3 max-w-lg leading-relaxed text-slate-400">{features[0].body}</p>
          <div class="mt-8 flex flex-wrap gap-2 text-sm">
            <span class="border border-white/10 px-3 py-1 text-slate-300">Svelte</span>
            <span class="border border-white/10 px-3 py-1 text-slate-300">Vite</span>
            <span class="border border-white/10 px-3 py-1 text-slate-300">Tailwind CSS</span>
          </div>
        </div>

        <div class="border border-indigo-300/20 bg-indigo-400/10 p-8 md:col-span-2">
          <h3 class="text-xl font-semibold text-white">{features[1].title}</h3>
          <p class="mt-3 leading-relaxed text-slate-300">{features[1].body}</p>
        </div>

        <div class="border border-white/10 bg-white/[0.03] p-8 md:col-span-6">
          <h3 class="text-xl font-semibold text-white">{features[2].title}</h3>
          <p class="mt-3 max-w-2xl leading-relaxed text-slate-400">{features[2].body}</p>
        </div>
      </div>
    </section>

    <!-- How it works -->
    <section id="how" class="scroll-mt-8 border-t border-white/10 py-24">
      <h2 class="max-w-2xl text-3xl font-bold tracking-tight text-white sm:text-4xl">
        From new server to running in three steps.
      </h2>
      <ol class="mt-12 grid gap-10 md:grid-cols-3">
        {#each steps as step, i}
          <li class="relative border-l border-white/15 pl-6">
            <span class="absolute -left-[5px] top-1.5 size-2.5 bg-indigo-300"></span>
            <h3 class="text-lg font-semibold text-white">{i + 1}. {step.title}</h3>
            <p class="mt-2 leading-relaxed text-slate-400">{step.body}</p>
          </li>
        {/each}
      </ol>
    </section>

    <!-- CTA -->
    <section class="mb-24 border border-white/10 bg-gradient-to-br from-indigo-500/15 to-transparent p-10 sm:p-14">
      <h2 class="max-w-xl text-3xl font-bold tracking-tight text-white sm:text-4xl">
        Neoactyl is still being built. Follow along.
      </h2>
      <p class="mt-4 max-w-xl text-slate-300">
        Try it, report bugs, or contribute on GitHub.
      </p>
      <div class="mt-8 flex flex-col gap-3 sm:flex-row">
        <a
          href="https://neoactyl.app/"
          target="_blank"
          rel="noopener noreferrer"
          class="inline-flex items-center justify-center bg-white px-7 py-3.5 font-semibold text-slate-900 transition hover:-translate-y-0.5 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-300"
        >
          Get started
        </a>
        <a
          href="https://github.com/neoactyl"
          target="_blank"
          rel="noopener noreferrer"
          class="inline-flex items-center justify-center border border-white/15 px-7 py-3.5 font-semibold text-white transition hover:bg-white/10 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-300"
        >
          Star on GitHub
        </a>
      </div>
    </section>
  </main>

  <footer class="mx-auto flex max-w-6xl flex-col items-center justify-between gap-4 border-t border-white/5 px-6 py-10 text-sm text-slate-500 sm:flex-row">
    <span class="font-medium text-slate-400">Neoactyl</span>
    <span>© 2026 Neoactyl</span>
  </footer>

  <footer class="border-t border-white/5 px-6 py-4 text-center text-sm text-slate-500">
    This website is just a prototype.
  </footer>
</div>