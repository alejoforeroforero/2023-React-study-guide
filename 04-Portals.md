1. Create a Div in index.html:

       <div id="modal-hook"></div>
       <div id="root"></div>
       
       
2. Create a component where the Div is called, the content should be passed:

       return ReactDOM.createPortal(content, document.getElementById('modal-hook'));
       
