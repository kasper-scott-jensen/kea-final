<script>
  import { Link } from 'svelte-routing'

  let date = new Date().getFullYear();

  export let absolute = false;
</script>

<footer
  class="pb-6 {absolute
    ? 'absolute w-full bottom-0 bg-blueGray-800'
    : 'relative'}"
>
  <div class="container mx-auto px-4">
    <hr class="mb-6 border-b-1 border-blueGray-600" />
    <div class="flex flex-wrap items-center md:justify-between justify-center">
      <div class="w-full md:w-4/12 px-4">
        <div
          class="text-sm text-blueGray-500 font-semibold py-1 text-center md:text-left"
        >
          Copyright {date} © Cronio
        </div>
      </div>
      <div class="w-full md:w-8/12 px-4">
        <ul class="flex flex-wrap list-none md:justify-end justify-center">
          <li>
            <Link to={'/'}>
              <a
                href="#"
                class="text-white hover:text-blueGray-300 text-sm font-semibold block py-1 px-3"
              >
                Home
              </a>
            </Link>
          </li>
          <li>
            <a
              href="https://github.com/kasperscottjensen"
              class="text-white hover:text-blueGray-300 text-sm font-semibold block py-1 px-3"
            >
              Source Code
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</footer>
