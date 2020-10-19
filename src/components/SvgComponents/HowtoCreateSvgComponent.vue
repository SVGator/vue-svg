## How to integrate an SVG exported from SVGator into Vue.js

### Step 1
Export from svgator.com

### Step 2
Create a blank VueJS file of format:

    <template>
    </template>
    
    <script>
    export default {
      name: "MyVueComponent",
      mounted() {
      },
    };
    </script>
    
### Step 3
Fill the content of the blank VueJS file from the exported SVG file:

    <template>
        <svg> ... </svg>
        // Practially the <script> tag is eliminated from the exported file
        // Important: Don't copy only the begining of the file content, since the closing </svg> tag is the last
    </template>
    
    <script>
    export default {
      name: "MyVueComponent",
      mounted() {
        // the content of the script tag comes here
        // Note1: the <script> and </script> tags doesn't have to be copied here
        // Note2: The <![CDATA[ from the beginning is not needed
        // Note3: The ]] from the end is also not needed
        // eg.:
        !function(t,n){.....
        this.__SVGATOR_PLAYER__.build({......
        // Important: The 2nd row of the JS code has to be prefixed w/ "this.":
        // __SVGATOR_PLAYER__ should be changed to this.__SVGATOR_PLAYER__
      },
    };
    </script>