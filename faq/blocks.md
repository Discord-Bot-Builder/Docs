---
description: About DBB Blocks System
---

# Blocks

Under construction...

## Blocks are the Action Tools of your Bot. 
They are created with node JS and a Basic Structur for `Name`, `Input`, `Options`, `Output` and the `code` Part.

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

2. The Inputs:
<details>
  <summary>Example</summary>
  
  These are The Inputs of your Block showed in DBB.
  
  ```javascript
    inputs: [
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
      ```
      
   </details>
   
</details>

3. The Options:
<details>
  <summary>Example</summary>
  
  ```javascript
    options: [
      
    ]
  ```
  
  #### The Option Types
  "type" supports SELECT, TEXT, COLOR and NUMBER
</details>

4. The Outputs:
<details>
  <summary>Example</summary>
  
  ```javascript
    outputs: [
    
    ]
  ```
</details>

5. The Code:
<details>
  <summary>Example</summary>
  In Sync
  
  ```javascript
    code: function(cache){
    
    }
  ```
  
  In Async
  
  ```javascript
    code: async function(cache){
    
    }
  ```
  
</details>

