- useState:

      const [variableName, fxToUpadate] = useState(true);

      const changeVariable = ()=>{

          if(variableName){
              fxToUpadate(false);
          }else{
              fxToUpadate(true);
          }
        
          console.log(variableName);
      }
