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
      
- useReducer:

      function inputReducer(state, action){
            switch(action.type){
            case 'CHANGE':
                  return {
                  ...state,
                  value:action.val,
                  isValid: true
                  }
            default:
            return state;
            }
      }
      
      const [inputState, dispatch] = useReducer(inputReducer, {value:'', isValid:false});
      
      function changeHandler(event){
        dispatch({type:'CHANGE', val:event.target.value})
      }
