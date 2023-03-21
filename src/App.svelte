<script>
  let login = '',
      password = '';
</script>
<main class="relative flex flex-col justify-center items-center min-h-screen">
  <h1 class="text-center text-5xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-yellow-300 to-red-600">
    41t</h1>

  <div class="relative">
    <form name="auth"
          on:submit={async (event) => {
          event.preventDefault();
          const res = await fetch('http://api.localhost/auth/login', {
            method: 'post',
            headers: {
              'Content-type': 'application/json'
            },
            body: JSON.stringify({ login, password })
          });
          console.log(res);
        }}
          class="z-10 relative backdrop-blur-2xl text-lg grid shadow-xl m-6 py-6 px-8 gap-6 bg-white/40 dark:bg-neutral-700/40 border border-neutral-50 dark:border-neutral-600 rounded-xl">

      <header>
        <h2 class="text-center text-3xl">Вход</h2>
      </header>
      <label for="login" class="space-y-2">
        <span class="block">Логин</span>
        <input id="login" name="login" placeholder="" required bind:value={login}
               class="outline-none duration-100 focus:ring focus:ring-amber-400/40 bg-neutral-100/50 dark:bg-neutral-800/50 px-4 py-2 border border-neutral-50 dark:border-neutral-600 focus:shadow-md focus:border-amber-300 hover:border-amber-300 rounded-xl">
      </label>

      <label for="password" class="space-y-2">
        <span class="block">Пароль</span>
        <input type="password" id="password" name="password" placeholder="" required bind:value={password}
               class="outline-none duration-100 focus:ring focus:ring-amber-400/40 bg-neutral-100/50 dark:bg-neutral-800/50 px-4 py-2 border border-neutral-50 dark:border-neutral-600 focus:shadow-md focus:border-amber-300 hover:border-amber-300 rounded-xl">
      </label>

      <button
          class="outline-none duration-200 text-neutral-900 justify-self-end px-4 py-2 bg-amber-400/80 shadow-md hover:shadow-amber-400 focus:ring focus:ring-amber-400/40 border border-amber-300 rounded-xl">
        Войти
      </button>
    </form>
    <div class="z-0 absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 blur-3xl">
      <div class="relative">
        <div class="w-48 h-48 absolute rounded-full bg-yellow-300/40 right-0 top-0"></div>
        <div
            class="w-96 h-96 absolute rounded-full bg-gradient-to-r from-yellow-300/40 to-red-600/40 -translate-x-1/2 -translate-y-1/2"></div>
        <div class="w-48 h-48 absolute rounded-full bg-red-600/40 bottom-0 left-0"></div>
      </div>
    </div>
  </div>
  <div class="bg-grid-slate-400 mask-image absolute top-0 right-0 bottom-0 left-0"></div>
</main>

<style>
  .bg-grid-slate-400 {
      background-image: url("./lib/angle.svg");
  }

  .mask-image {
      mask-image: radial-gradient(black, transparent);
  }
</style>