

function comenzar(){
    var boton =document.getElementById("grabar");
    boton.addEventListener("click", itemNuevo, false);
}

function itemNuevo(){
    var clave=document.getElementById("clave").value;
    var valor=document.getElementById("valor").value;
    localStorage.setItem(clave, valor); 
    //sessionStorage[clave]= valor;
    leer_mostrar(clave); 
    document.getElementById("clave").value="";
    document.getElementById("valor").value="";
}

function leer_mostrar(clave){
    var zonadatos=document.getElementById("zonadatos");
    zonadatos.innerHTML='<div><button onclick="elimnarTodo()">Eliminar Todo </button></div>';
    //var elvalor=sessionStorage.getItem(clave);
    //var elvalor=sessionStorage[clave];
    //zonadatos.innerHTML="";
    for(i=0;i<localStorage.length;i++){
        var clave=localStorage.key(i);
        var elvalor=localStorage.getItem(clave);
        zonadatos.innerHTML+='<div>Clave: ' + clave + '<br>' + 'Valor: ' + elvalor + '<br><button onclick="eliminarItem(\'' + clave + '\')">Eliminar</button></div>';
         }
} 

function elimnarTodos() {
    if (confirm("Estas Seguro?")){
        localStorage.clear();
        leer_mostrar();
    }
}

function eliminarItem(clave){
    if (confirm("Estas Seguro?")){
        localStorage.removeItem(clave);
        leer_mostrar();
    }
}
window.addEventListener("load", comenzar, false);