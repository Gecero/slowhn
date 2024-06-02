# SlowHN
A slow, static site interface for Y Combinator's Hacker News. For a customized, daily updated instance, see [this](https://gecero.de/h/).   

SlowHN is a toolchain that is composed out of three steps and tools. To run them, you will need golang, curl, bash and jq.   
1. Fetch HNs 'top' page entries for yesterday (``fetch``)
2. Turn the JSON into an HTML table (``tohtml``)
3. Insert that table into an existing HTML file (``htmled``)

## Installation
To get started, run these commands:
```bash
git clone https://github.com/gecero/slowhn
cd slowhn
# Install htmled, which is not included in this repo
go install github.com/gecero/mariurss/htmled@latest
```

## Usage
The intended usage for these tools looks like this:
```bash
# This will put the SlowHN table into index.html's div #slowhn-content
./fetch | ./tohtml | htmled index.html "#slowhn-content"
```

