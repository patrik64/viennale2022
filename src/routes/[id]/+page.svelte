<!--script context="module">
    // @ts-ignore
    export const load = ({ params }) => {
      const id = params.id;
  
      return {
        props: {
          id
        }
      };
    };
  </script-->
  
  <script>
    export let data;
    let id = data[0];

    import movies from "$lib/data/movies.json";
  
    let movie = movies[id - 1];
  </script>
  
  <div class="my-10 mx-auto lg:w-1/2 bg-white shadow overflow-hidden sm:rounded-lg">
    <div class="px-4 py-5 sm:px-6">
      <div class="text-2xl leading-6 font-medium">{movie.name}</div>
      {#if movie.image && movie.image.length > 0}
        <img class="my-4 object-contain" src={`/images/movies/${movie.image}`} alt="" />
        <div class="text-xss text-gray-500">&copy; imdb</div>
      {/if}
    </div>
    <div class="border-t border-gray-200 px-4 py-5 sm:p-0">
      <dl class="sm:divide-y sm:divide-gray-200">
        <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
          <dt class="text-sm font-medium text-gray-600">Name</dt>
          <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">{movie.name}</dd>
        </div>
        <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
          <dt class="text-sm font-medium text-gray-600">IMDB Score</dt>
          <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">{movie.score}</dd>
        </div>
        <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
          <dt class="text-sm font-medium text-gray-600">IMDB</dt>
          <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2"><a href={movie.links[1].lvalue} class="hover:text-black">{movie.links[1].lvalue}</a></dd>
        </div>
        <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
          <dt class="text-sm font-medium text-gray-600">Viennale</dt>
          <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2"><a href={movie.links[0].lvalue} class="hover:text-black">{movie.links[0].lvalue}</a></dd>
        </div>
        <!--div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
          <dt class="text-sm font-medium text-gray-600">Sterbedatum</dt>
          <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">{person.deathdate}</dd>
        </div>
        <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
          <dt class="text-sm font-medium text-gray-600">Sterbeort</dt>
          <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">{person.deathplace}</dd>
        </div>
        <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
          <dt class="text-sm font-medium text-gray-600">Funktion / Rolle</dt>
          {#if person.role.length > 0}
            <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">{person.function} / {person.role}</dd>
          {:else}
            <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">{person.function}</dd>
          {/if}
        </div>
        {#if person.links.length > 0}
          <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
            <dt class="text-sm font-medium text-gray-600">Links</dt>
            <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">
              <ul>
                {#each person.links as link}
                  <li class="py-1">
                    <a rel="external" href={link.lvalue} class="text-teal-400">{link.lkey}</a>
                  </li>
                {/each}
              </ul>
            </dd>
          </div>
        {/if}-->
      </dl>
    </div>
  </div>
  