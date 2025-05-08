
# Curl Commands for API Usage

## 1. View/Download/Post Using APIs
To view the data returned by an API:
```bash
curl https://catfact.ninja/fact
```

## 2. Download the Data to a File
To download data from a URL and save it to a file rather than showing it in the terminal:
```bash
curl -o <filename> <url>
```

## 3. Acting as a Browser
To mimic a browser request:
```bash
curl --user-agent="Mozilla/5.0" -O <name> <url>
```
OR
```bash
curl -A "Mozilla/5.0" -o <nametogive> <url>
```

## 4. Posting Data
To send a POST request with JSON data:
```bash
curl -X POST <url> \
-H "Content-Type: application/json" \
-d <data>  # or -d @<filename with data>
```
