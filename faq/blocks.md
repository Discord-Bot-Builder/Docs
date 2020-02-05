---
description: About DBB Blocks System
---

# Blocks

Under construction...

## Blocks are the Action Tools of your Bot. 
They are created with node JS and a Basic Structur for `name`, `inputs`, `options`,`output` and the `code` Part.

---

## How to Submit to DBB
Its easy if you want to use them Only by yourself just Place the JS file in your Bot Directry and go on. If everything is ok with the file its getting Loaded instand without restarting DBB.

Only if modifications on the File made that interacts with the Block (not the `code` part) DBB needs to be Restarted.

---

## The Line Types

If you worked with DBB already you know that there are some Different colors for lines. These are to make it easyer for you to see what can be connected (is the same type of var) and not only for the Style :D.

The differen types are:
` unspecified, undefined, null, object, boolean, number, text, list, date, action `

How to use them we'll see later.

---

### The Basic Structure

1. The default Structure:
<details>
  <summary>The full Preview:</summary>
  
  This Structur is the Block that get Showed in DBB Ther you can Place Stuff like Name, Description, Category and more.
  Please make shure that you arent use the Same name for to Blocks!
  
  ```javascript
  module.exports = {
    name: "",

    description: "",

    category: "",

    auto_execute: true,

    inputs: [],

    options: [],

    outputs: [],
    
    code: function(cache) {
        
    }
};
  ```
  
  *Note: Gold* **loves** *to see the the brake between the Object Keys ;), Simply add them befor sending it to him.* 
</details>

2. The Inputs and Outputs:
<details>
  <summary>Example</summary>
  
  These are The Inputs and Outputs of your Block showen in DBB.
  *If you Update Something here Please Restart DBB to see it there.*
  
  ```javascript
    inputs/outputs: [
      {
            "name": "",
            "title": "",
            "description": "",
            "types": []
        }
    ]
    // types : unspecified, undefined, null, object, boolean, number, text, list, date, action
  ```  
  
  In the `name` fild gets the Name of the variable used in the code section. Please make shure that the names are Unique for the File.
  
  `title` is the Name how it shown in DBB itself.
  
  `description` is the Text that Pops up if you Hover on the Connectionpoint in DBB. Helpfull to Descripe the Types here ;).
  
  `types` is an Array of Types that can be Connected here. If you want only one Type to be Connected use `[ "yourtype" ]` if you need more use a comma seperated list inside the `[]` like this `[ "unspecified", "undefined", "null", "object" ]`.
   
   The `inputs` field is an Array of Objects. That mean you can Add as many Inputs you need by Cloning the Object and add it again. To make it valid **between** the Objects there **needs** to be a `,`. Thats for all Type of Field from Type are Array!!!
   
   <details>
      <summary>Example</summary>
      
      ```javascript
      inputs: [
        {
            "name": "action",
            "title": "Action",
            "description": "Acceptable Types: Action\n\nDescription: Executes this block.",
            "types": ["action"]
        },
        {
            "name": "value",
            "title": "Value",
            "description": "Acceptable Types: Unspecified, Undefined, Null, Object, Boolean, Number, Text, List\n\nDescription: What it actually used for.",
            "types": ["unspecified", "undefined", "null", "object", "boolean", "number", "text", "list"]
        }
      ]
      
      ...
      
      outputs: [
        {
            "name": "action",
            "title": "Action",
            "description": "Type: Action\n\nDescription: Executes blocks.",
            "types": ["action"]
        }
      ]
      ```
      
      ]
   </details>
   
</details>

3. The Options:
<details>
  <summary>Example</summary>
  
  These are the Options of your Block showen in DBB.
  *If you Update Something here Please Restart DBB to see it there.*
  
  #### Basic Options
  
  ```javascript
    options: [
      {
            "name": "",
            "title": "",
            "description": "",
            "type": ""
        }
    ]
  ```
  
  ##### The Option Types
  `type` supports `SELECT, TEXT, COLOR, NUMBER`
  
  By `type` => `COLOR` it will appere the Color-Picker to select a Color. 
  *Note: Gold loves his Color-Picker, like it to and he likes you back ;D*
  
  By `type` => `TEXT` or `NUMBER` a Field to type your Value in shows on the Block in DBB. 
  
  By `type` => `SELECT` a Dropdown Menu will be shown in DBB.
  
  If you use any other then `SELECT` you are fine with this Options Structure.
  By `SELECT` you need to add the `options` field to the `options` Object. (yea sounds wired, just go on :D ) 
  The new `options` filed is an Array of Items.
  
  ```javascript
  /** value for code => */ 0 : "Option to Select" /** <= Shown in DBB */
  ```
  
  ###### The `options` in `options` array Example:
  
  ```javascript
    options:[
      {
        "name": "",
        "title": "",
        "description": "",
        "type": "SELECT",
        "options": [
          0 : "Option to Select 1",
          1 : "Option to Select 2",
          ...
        ]
      }
    ]
  ```
  


</details>

4. The Code:
<details>
  <summary>Example</summary>
  
  The One and the only part that do something in your Bot.
  *All above is just to show it in the DBB Editor right.*
  
  For this Stuff you need some knowledge in Javascript.
  You can do mostly anything here.
  
  DBB always await the end of the Function. 
  
  
  ```javascript
    code: function(cache){
    
    }
  ```
  ##### The `cache` Object
  
  The `cache` Object includes the Information arround the Block. Without this its useless.
  *You only need it for the included funktions from **this**.*
 
  <details>
  
  <summary>Example</summary>
  
  ```javascript
  {
  "name":"join_voicechannel",
  "index":"",
  "workspace":"",
  "inputs":{},
  "outputs":{}
  }
  ```
  `name` is the Block Name itself.
  `index` is the Number of the Block (out of DBB).
  `workspace` is a Number what it mean... IDK :=).
  `inputs` is the Array of your Input lines (only the ID's of the Line gets here).
  `outputs` is an Array of your Output Lines (only the ID's too).
  
  </details>
  
  ##### The `this` Object
  
  The `this` Object includes all activ Blocks (you **don't** need this) and some usefull Functions for you.
   
  ```javascript
  // Usefull stuff for you!!
  this.GetInputValue("linename", cache);
  this.GetOptionValue("linename", cache);
  this.StoreOutputValue("value", "linename", cache);
  this.RunNextBlock("linename", cache);
  this.require("modul");
  // Just ignore anything else ;)
  ```
  
  With this functions you can get or store the Input-, Option- and Outputvalues or run the next Block. (With the right function.
  
  
  For Example here is the code Block from the Print Action.
  
  ```javascript
  code: function(cache) {
    const content = this.GetInputValue("value", cache);

    console.log(content);
    
    this.RunNextBlock("action", cache);
  }
  ```
  
  `"value"` in `this.GetInputValue()` is defined in the `inputs` part of the Block.
  
  <details>
    <summary>Input Object from Block</summary<
    
    ```javascript
    inputs: [
        {
            "name": "action",
            "title": "Action",
            "description": "Acceptable Types: Action\n\nDescription: Executes this block.",
            "types": ["action"]
        },
        {
            "name": "value",
            "title": "Value",
            "description": "Acceptable Types: Unspecified, Undefined, Null, Object, Boolean, Number, Text, List\n\nDescription: The value that you want to send to your console.",
            "types": ["unspecified", "undefined", "null", "object", "boolean", "number", "text", "list"]
        }
    ]
    ```
  </details>
  
  `"action"` in `this.RunNextBlock()` is defined in the `outputs` part of the Block.
  
  <details>
    <summary>Output Object from Block</summary<
    
    ```javascript
    outputs: [
      {
        "name": "action",
        "title": "Action",
        "description": "Type: Action\n\nDescription: Executes blocks.",
        "types": ["action"]
      }
    ]
    ```
  </details>
  
  ##### `Modul loading with this.require()`
  
  If you want to import an Module like `fs` or `path` that **aren't** downloaded **from npm**, simpley use it like anywhere else, just put it inside the `code` Field:
  
  <details>
    <summary>Example</summary<
    
    ```javascript
    code : function(cache){
      const path = require("path");
      // and go on like you wan't...
    }
    ```
  </details>
  
  If you want to import an Module like `discord.js` **from npm** please use `this.require()` like this:
  
  <details>
    <summary>Example</summary<
    
    ```javascript
    code : function(cache){
      const discord = this.require("discord.js");
      // and go on :)
    }
    ```
  </details>
  
  To improve Performance you should only use Default packages and if you need another try to use a minimal libary of this function.
</details>

