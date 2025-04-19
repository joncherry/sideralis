1. Install mermaid-cli with npm. https://github.com/mermaid-js/mermaid-cli `npm install -g @mermaid-js/mermaid-cli`
2. Then follow the solution in this issue on the repo https://github.com/mermaid-js/mermaid-cli/issues/764 for me the file was at `~/node-v23.11.0-linux-x64/lib/node_modules/@mermaid-js/mermaid-cli/src/index.js`
3. for mdi icons use step 2 but use this so the url is for mdi
```js
mermaid.registerIconPacks([
              {
                 name: 'mdi',
                 loader: () =>
                   fetch('https://unpkg.com/@iconify-json/mdi@1.2.3/icons.json').then((res) => res.json()),
               },
             ]);
```
4. Then run this command after replacing {name} `mmdc -i ./Internal_Documentation/design/{name}.mmd -o ./Internal_Documentation/design/{name}.svg -t dark --backgroundColor black`