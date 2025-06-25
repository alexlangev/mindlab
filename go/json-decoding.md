## 2 ways to go from JSON to go

### json.Decoder(stream)

Processes JSON data incrementally as a stream. This is particularly useful for large JSON payloads or when reading JSON directly from a network connection or file. It avoids loading the entire JSON into memory at once, making it more memory-efficient, although potentially slower due to the streaming nature.

We get JSON like this from an HTTP request. Let's convert into a go struct.
```JSON
[
  {
    "id": "001-a",
    "title": "Unspaghettify code",
    "estimate": 9001
  }
]
```

To decode this JSON into a slice of Issue structs, we need to know the JSON fields and their types.
The standard encoding/json package uses tags to map JSON fields to struct fields.
The struct fields needs to be exported (capitalized)

```go
type Issue struct {
	Id       string `json:"id"`
	Title    string `json:"title"`
	Estimate int    `json:"estimate"`
}

// res is a successful `http.Response`

var issues []Issue
decoder := json.NewDecoder(res.Body)
if err := decoder.Decode(&issues); err != nil {
    fmt.Println("error decoding response body")
    return
}

// Can now do stuff with issues
for _, issue := range issues {
    fmt.Printf("Issue – id: %v, title: %v, estimate: %v\n", issue.Id, issue.Title, issue.Estimate)
    // Issue – id: 001-a, title: Unspaghettify code, estimate: 9001
}
```

### json.Unmarshal (one chunk)
