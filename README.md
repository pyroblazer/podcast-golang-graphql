# podcast-golang-graphql

After editing the schema.graphqls, run 

```
go run github.com/99designs/gqlgen generate
```

Then, run the GraphQL server locally
```
go run .
```

Sample Queries
```
query Search {
  search(term:"Full StackRadio") {
    artist
    podcastName
    episodesCount
  }
}

query Feed {
  feed(feedUrl: "https://feeds.simplecast.com/Gd37VcDw") {
    title
    image
    linkUrl
  }
}
```