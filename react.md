
#CURSO DE REACT JS.


##INSTALACIÓN DE REACT Y REACT DOM.
    npm init 
    instrucciones (nombre, version, desc, endpoint, test, git)
    npm install react react-dom
    crear estructura.
    carpeta 
    src / 
    index.js 
	    /components 
	    / App.jsx
    carpeta public / 
    index.html

                /// Ejemplo para hacer el index


                import React from 'react';
                import ReactDOM from 'react-dom';

                ReactDOM.render(<App />, document.getElementById('app'));

                App.jsx

                import React from 'react';

                const App = () => {
	                return (
		                <h1>Hola Mundo!</h1>
	                );
                }

                export default App;

                ///
-----
##INSTALACIÓN DE WEBPACK Y BABEL.
    npm install @babel/core @babel/present-env @babel/present-react


 


