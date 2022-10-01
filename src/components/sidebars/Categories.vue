<template>
  <div className="w-full flex flex-col my-4">
    <p class="text-xl font-semibold pb-5">SUBSCRIBE</p>
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
    <p class="title-font text-lg font-medium mb-3">CATEGORIES</p>
    <nav class="list-none mb-5">
      <ul v-for="category in $static.category.edges">
        <li>
          <g-link :to="category.node.path">{{ category.node.title | capitalise }} ({{ category.node.belongsTo.totalCount }})</g-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

<static-query>
query {
  category: allCategory(sortBy: "title", order: ASC) {
    edges {
      node {
        id
        title
        path
        belongsTo {
          totalCount
        }
      }
    }
  }
}
</static-query>