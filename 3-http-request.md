           const [cardsData, setData] = useState([]);
           
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
           
           
- Don't forget to check headers in the backend for avoiding CROSS problems:

            app.use((req, res, next)=>{
                      res.setHeader('Access-Control-Allow-Origin', '*');
                      res.setHeader('Access-Control-Allow-Headers', 'Origin, X-Requested-With, Content-Type, Accept, Authorization');
                      res.setHeader('Access-Control-Allow-Methods', 'GET, POST, PATCH, DELETE')
                      next();
            })
