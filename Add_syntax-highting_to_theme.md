Locate your VScode folder on your system, and find the "extension" folder.
`.../Microsoft VS Code\resources\app\extensions`

This folder contains the themes, and extensions you have, locate your favoriate theme.
`./theme-abyss`

Inside this folder you will see.
```
themes : folder
package.json
packet.nsl.json
```

open the themes folder and open the `abyss-color-theme.json` file in your favorite text editor
inside it might not be formatted, you have two options.

Option 1:
    At the beginning of the file you'll see `{"name": "Abyss","tokenColors": [{`
    Press enter at the `{` now you can continue to the next part.
    next you can customise the colours of the syntax highlighting as you want.

Option 2:
    Open the extentions tab (`Ctrl+shift+x`) and search json.
    Download `Json - Beautify JSON by meezilla`
    Open the `abyss-color-theme.json` file and press `Ctrl+shift+j`
    This will automatically formate the JSON for you. Then you can follow the next steps as you wnat.

Adding the Syntax highlighting

The Batasm language file is a little messy, so the following is all the formatting you can do
`nop, hlt` : `keyword.misc.Batasm`
`ldi, lod, mov, str` : `keyword.data.Batasm`
`adi, add, sub, xor, nor, and, not, neg, lsh. rsh, cmp, inc, dec` : `keyword.alu.Batasm`
`brh, jmp, cal, ret` : `keyword.brh.Batasm`
`R0 -> R9` : `keyword.registersd.Batasm`
`R10 -> R15` : `keyword.registersdd.Batasm`
`eq, ne, ge, lt` : `keyword.comparison.Batasm`
`.main or any .some` : `keyword.Func.Batasm`
`;, /, //` : `keyword.comment.Batasm`
`'Single quote strings'` : `string.quoted.Batasm` or `"string.quoted"`
Numbers : `constant.numeric`

To add your own colour to any of these just follow this easy step in your

```
{
    "name" : "Change all the branch instructions to bright red",
    "scope" : [
        "keyword.brh.Batasm"
    ],
    "setting" : {
        "foreground": "#ff0000",
		"fontStyle": "bold"
    }
},
```

You can now chnage the colour of the syntax!!!
To make more then one Token listed above the same colour, just add a `,` to the last one and add it!

```
"scope" : [
    "keyword.misc.Batasm`",
    "keyword.brh.Batasm"
]
```


Once you have made change the colours to how you like, after saving you can close and reopen VScode and the changes will show in any .as configured to Batasm!!

If you don't like the colours you picked, or like the defualt ones more, inside the `tokenColors` scope, you can find `Variable` and `Class name` that all have the defualt code colours!! To find the colours you like from other languages use `ctrl+shift+p` and in the top bar, search `developer: inspect editor tokens and scopes`, then highlight the colours you want!!

Watch this video for more help and a visual demonstrations!
https://youtu.be/Su-cNLe0dgw?si=UbOy1dxsqHYIaRhh