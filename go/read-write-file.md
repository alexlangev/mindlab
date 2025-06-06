You can write and read files with the **os** module

## Write

```go
// save a .json file
// 0644 is the linux permission value
func (l *List) Save(filename string) error {
	js, err := json.Marshal(l)

	if err != nil {
		return err
	}

	return os.WriteFile(filename, js, 0644)
}
```

## READ

```go
// read file from os
func (l *List) Get(filename string) error {
	file, err := os.ReadFile(filename)

	if err != nil {
		if errors.Is(err, os.ErrNotExist) {
			return nil
		}
		return err
	}

	if len(file) == 0 {
		return nil
	}

	return json.Unmarshal(file, l)
}
```
