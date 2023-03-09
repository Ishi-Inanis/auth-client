<script>
</script>

<main class="flex flex-col justify-center items-center min-h-screen">
  <h1 class="text-center text-5xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-yellow-300 to-red-600">
    41t</h1>
  <form action="" name="auth"
        class="text-lg grid shadow-xl m-6 py-6 px-8 gap-6 bg-white/40 dark:bg-neutral-700/40 border border-neutral-50 dark:border-neutral-600 rounded-xl">
    <header>
      <h2 class="text-center text-3xl">Вход</h2>
    </header>
    <label for="login" class="space-y-2">
      <span class="block">Логин</span>
      <input id="login" name="login" placeholder="" required
             class="outline-none duration-100 focus:ring focus:ring-amber-400/40 bg-neutral-100 dark:bg-neutral-800 px-4 py-2 border border-neutral-50 dark:border-neutral-600 focus:shadow-md focus:border-amber-300 hover:border-amber-300 rounded-xl">
    </label>

    <label for="password" class="space-y-2">
      <span class="block">Пароль</span>
      <input type="password" id="password" name="password" placeholder="" required
             class="outline-none duration-100 focus:ring focus:ring-amber-400/40 bg-neutral-100 dark:bg-neutral-800 px-4 py-2 border border-neutral-50 dark:border-neutral-600 focus:shadow-md focus:border-amber-300 hover:border-amber-300 rounded-xl">
    </label>

    <button
        class="outline-none duration-100 text-neutral-900 justify-self-end px-4 py-2 bg-amber-400/80 shadow-md hover:shadow-amber-400 focus:ring focus:ring-amber-400/40 border border-amber-300 rounded-xl">
      Войти
    </button>
  </form>
</main>