<template>
  <footer class="bg-background-secondary body-font">
    <div
      class="
        container
        px-5
        py-10
        md:py-24
        mx-auto
        flex
        md:items-center
        lg:items-start
        md:flex-row md:flex-nowrap
        flex-wrap flex-col
      "
    >
      <div class="flex-grow flex flex-wrap md:text-left text-center">
        <div class="lg:w-1/4 md:w-1/2 w-full px-4">
          <h2 class="title-font text-lg font-medium mb-3">QUICK LINKS</h2>
          <nav class="list-none mb-5">
            <ul>
              <li>
                <g-link to="/about/">About Us</g-link>
              </li>
              <li>
                <g-link to="/about/">Episodes</g-link>
              </li>
              <li>
                <g-link to="/subscribe/">Subscribe</g-link>
              </li>
              <li>
                <g-link to="/support/">Support</g-link>
              </li>
              <li>
                <g-link to="/resources/">Resources</g-link>
              </li>
            </ul>
          </nav>
        </div>
        <div class="lg:w-3/4 md:w-1/2 w-full px-8">
          <h2 class="title-font text-lg font-medium mb-3">ABOUT THE SHOW:</h2>
          <div class="mb-5">
            <p>
              It's May 1864, and the Union enters its fourth year of war against the Confederacy succession. Ulysses S. Grant -- Hero of Vicksburg -- has been promoted to General-in-Chief of the entire Union Army by President Lincoln in a last-ditch effort to win the war. Grant, placing his command in the field with the Army of the Potomac, will now execute his own aggressive strategy against the rebels on all fronts. But first, he must spend the next 47-days fighting his way across the enemy-held Commonwealth of Virginia. Join amateur historian and US Navy veteran Kyle M. Bondo, as he follows the history of Grant's Overland Campaign from Washington, DC, to Petersburg, Virginia, in War Yankee, an American Civil War Podcast is a history podcast presented by Gagglepod.
            </p>
          </div>
        </div>
      </div>
      <div
        class="
          w-64
          flex-shrink-0
          md:mx-0
          mx-auto
          mb-5
          md:-mb-5 md:mt-0
          mt-5
          text-center
          md:text-left
        "
      >
        <a
          class="
            flex
            title-font
            font-medium
            items-center
            md:justify-start
            justify-center
            text-gray-900
          "
        >
          <span class="site-logo"><site-logo /></span>
        </a>
        <!-- <p class="mt-2 text-sm">
          {{ $static.metadata.siteDescription }}
        </p> -->
        <div>&nbsp;</div>
        <nav class="list-none mb-5">
            <ul>
              <li>
                <g-link to="https://waryankee.libsyn.com/rss">Download RSS</g-link>
              </li>
              <li>
                <g-link to="https://podcastindex.org/podcast/452056">Podcast Index</g-link>
              </li>
              <li>
                <g-link to="https://podcasts.apple.com/us/podcast/war-yankee/id1522169260">Apple Podcasts</g-link>
              </li>
              <li>
                <g-link to="https://podcasts.google.com/u/1/feed/aHR0cHM6Ly93YXJ5YW5rZWUubGlic3luLmNvbS9yc3M">Google Podcasts</g-link>
              </li>
              <li>
                <g-link to="https://open.spotify.com/show/0ZUjVf8xGNunKioJR2nGes">Spotify</g-link>
              </li>
            </ul>
          </nav>
      </div>
    </div>
    <div class="bg-background-tertiary">
      <div
        class="container mx-auto py-4 px-5 flex flex-wrap flex-col sm:flex-row"
      >
        <!-- <p class="text-sm text-center sm:text-left">
          {{ `© ${new Date().getFullYear()} ${$static.metadata.siteName}` }} —
          <a
            :href="$static.metadata.siteAuthorUrl"
            rel="noopener noreferrer"
            class="text-gray-500 ml-1"
            target="_blank"
            >{{ `@${$static.metadata.siteAuthor}` }}</a
          >
        </p> -->
        <p class="text-sm text-center sm:text-left">
          {{ `© Copyright ${new Date().getFullYear()}. War Yankee and Gagglepod. All Rights Reserved.` }}</p>
        <!-- <span
          class="
            inline-flex
            sm:ml-auto sm:mt-0
            mt-4
            justify-center
            sm:justify-start
          "
        >
          <a
            :href="$static.metadata.siteAuthorUrl"
            target="_blank"
            rel="noopener noreferrer"
            class="text-gray-500"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              fill="currentColor"
              class="bi bi-github"
              viewBox="0 0 16 16"
            >
              <path
                d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"
              />
            </svg>
          </a>
        </span> -->
      </div>
    </div>
  </footer>
</template>

<static-query>
query {
  metadata {
    siteName
    siteDescription
    siteAuthor
    siteAuthorUrl
  }
}
</static-query>

<script>
export default {
  components: {
    SiteLogo: () => import('~/components/SiteLogo.vue'),
  },
}
</script>
