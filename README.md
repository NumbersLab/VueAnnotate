# Welcome to VueAnnotate !

The goal is to **Simplify** the writing of [VueJS](https://github.com/vuejs/vue). The files are entirely in TypeScript.

# Files

Only **Two files are required.** :
1. VueAnnotate.ts
2. VueCompat.ts.

## Exemple 

      @VueClass()  
      export default class ClassName extends Vue {  
       
	      @VueVar(true)  
	      bool: boolean;  
      
	      @VueVar('Hello World')
	      s:string;
        
	      @VueVar({country: 'France', population: 66000000})  
	      obj: { country: string, population: number };  
      
	      @Autowire(Repository.name)  
	      repo: Repository;  
	      
      }
