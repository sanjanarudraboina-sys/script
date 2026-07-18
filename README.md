function addStudent(){

    let name=document.getElementById("name").value;
    let age=document.getElementById("age").value;
    let course=document.getElementById("course").value;

    if(name=="" || age=="" || course==""){
        alert("Fill all fields");
        return;
    }

    let table=document.getElementById("studentList");

    let row=table.insertRow();

    row.insertCell(0).innerHTML=name;
    row.insertCell(1).innerHTML=age;
    row.insertCell(2).innerHTML=course;

    let btn=document.createElement("button");
    btn.innerHTML="Delete";
    btn.className="delete";

    btn.onclick=function(){
        row.remove();
    };

    row.insertCell(3).appendChild(btn);

    document.getElementById("name").value="";
    document.getElementById("age").value="";
    document.getElementById("course").value="";
}
