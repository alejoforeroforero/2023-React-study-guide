          useEffect(()=>{
                  const sendRequest = async()=>{
                      try{
                          const response = await fetch('http://localhost:3000/api/');
                          const responseData = await response.json();

                          setData(responseData);
                      }catch(error){
                          console.log(error);
                      }            
                  }  

                  sendRequest();
              }, [])
