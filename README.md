# Welcome to VueAnnotate !

The goal is to **Simplify** the writing of [VueJS](https://github.com/vuejs/vue). The files are entirely in TypeScript.

# Files

Only **Two files are required.** :
1. VueAnnotate.ts
2. VueCompat.ts.

# Exemple 

    $(document).ready(function(){
          
          var ClassName = new Vue({  
              el: '#id', 
	          data: {  
	              bool: 'true',
	              s: 'Hello World',
	              obj: {country: 'France', population: 66000000}
	          }
	          methods:{  
			     foo:function () {  
			         return true;  
			     }
			  }

Become :

    @VueClass()  
    export default class ClassName extends Vue {  
       //Variable used in View + Init
	    @VueVar(true)  
	    bool: boolean;  
      
	    @VueVar('Hello World')
	    s:string;
        
	    @VueVar({country: 'France', population: 66000000})  
	    obj: { country: string, population: number };
		  
		constructor(container: string, vueDataConstructor: any = null) {  
			super(vueDataConstructor);
		}
    	
    	//Function	  
    	foo() {  
    		return true;  
	    }
	}
    let className = new ClassName('#id');
