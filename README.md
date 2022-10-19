# jspractise
<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">

    <style>

      #bap{
max-height: 130px;
border:1px solid red;
display: flex;
overflow-x:scroll;

scrollbar-width:none;

      }
      #item{
min-width: 100px;
height: 100px;
text-align: center;
background: lightblue;
line-height: 100px;
margin-right: 3px;


      }

#sidebar{
  position: absolute;
right:36px;
animation:exam 1s; 

}

@keyframes exam {


    0% {
   right: 0%;
   
  }
  50% {

    right: 36px;
  }  
}




.bbbox{
width: 237px; height: 33px; 
text-align: center;
margin: auto;
}

.bbox{
text-align: center;margin: auto;

width: 237px; height: 150px; border:1px solid yellow;
}


.row {
  --bs-gutter-x: 0 !important;
}
</style>
  </head>
  <body>
  






<div id="bap"> 

<div id="item">1</div>
<div id="item">2</div>
<div id="item">3</div>
<div id="item">4</div>
<div id="item">4</div>
<div id="item">5</div>
<div id="item">6</div>
<div id="item">7</div>
<div id="item">8</div>
<div id="item">9</div>
<div id="item">0</div>
 </div>



    <!-- Optional JavaScript; choose one of the two! -->

<div>
  <canvas id="myChart"></canvas>
</div>
<input type="date" name="" id="cal1" onchange="fil()">
<input type="date" name="" id="cal2" onchange="fil()">
<br>
<br>

<div>
  <p>hdsh</p>
  



</div>

<div id="load" style="display:none;height:100px;width:200px;border:2px solid red;margin: auto;">
  

<div class="row">
  <div class="col-4" id="div1"style="border:1px solid red;height:50px;"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTvMmpS1UuWBMnfPK8UU3Lk3mTvwgSLyqX11A&usqp=CAU"style="width:60%;"></div>
  <div class="col-4" id="div1"style="border:1px solid red;height:50px;"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTBAZDYcFsx1DJuJOZcjvKfw8e1NEemupgILw&usqp=CAU"style="width:53%;"></div>
  <div class="col-4" id="div1"style="border:1px solid red;height:50px;"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRzAaFlSuKJ8ei9Xv2quXNPN-GSowMOLm3S6Q&usqp=CAU"style="width:67%;"></div>


</div>

<div class="row">
  <div class="col-4" id="div1"style="border:1px solid red;height:50px;"><img src="https://cdn.pixabay.com/photo/2014/04/02/10/43/mango-304315__340.png"style="width:62%;"></div>


  <div class="col-4"id="div1"style="border:1px solid red;height:50px;"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSdzFdQjm52lXgmyZ6t5bESmnbmZpD1CpJXkg&usqp=CAU"style="width:73%;"></div>
  <div class="col-4"id="div1"style="border:1px solid red;height:50px;"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSO83K0waIJh30bpgoDwVNRxdj8xMCjxkLTdg&usqp=CAU"style="width:73%;"></div>
</div>
</div>

<p class="text-center"id="pp"style="font-weight: 600"></p>


<div style="width:200px;height: 30px;border: 2px solid green;margin: auto;"id="daddiv"><div style="height:12px;border: 2px solid red;"id="score"></div></div>





<div id="mydrag" style="height:39px;width:22px;border: 2px solid red;"></div>



<input type="text" name=""id="inn">
<input type="range"id="ra"Max="10"min="1">



<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

    <script >

//randomindex end

const randomizeIndex = (count) => {
    return Math.floor(count * Math.random());
};
//randomindex end

//randomarray end
var aaa=[]
const randarray=(arr,count)=>{
if(count>arr.length){

  throw new Error("count can't be greater than arraylength ");
}
let res=[];
let setsindex=new Set();
while(res.length<count){
let index=randomizeIndex(count);
if(setsindex.has(index)){
  continue;
}


let ele=arr[index]
setsindex.add(index)
res.push(ele)

}
aaa=[...res]
return aaa;
}
//randomarray end
var e=["https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTvMmpS1UuWBMnfPK8UU3Lk3mTvwgSLyqX11A&usqp=CAU","https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTBAZDYcFsx1DJuJOZcjvKfw8e1NEemupgILw&usqp=CAU","https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRzAaFlSuKJ8ei9Xv2quXNPN-GSowMOLm3S6Q&usqp=CAU","https://cdn.pixabay.com/photo/2014/04/02/10/43/mango-304315__340.png","https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSdzFdQjm52lXgmyZ6t5bESmnbmZpD1CpJXkg&usqp=CAU","https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSO83K0waIJh30bpgoDwVNRxdj8xMCjxkLTdg&usqp=CAU"]
var e2=["https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTvMmpS1UuWBMnfPK8UU3Lk3mTvwgSLyqX11A&usqp=CAU","https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTBAZDYcFsx1DJuJOZcjvKfw8e1NEemupgILw&usqp=CAU","https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRzAaFlSuKJ8ei9Xv2quXNPN-GSowMOLm3S6Q&usqp=CAU","https://cdn.pixabay.com/photo/2014/04/02/10/43/mango-304315__340.png","https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSdzFdQjm52lXgmyZ6t5bESmnbmZpD1CpJXkg&usqp=CAU","https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSO83K0waIJh30bpgoDwVNRxdj8xMCjxkLTdg&usqp=CAU"];

console.log(aaa)
//1,2,3,4 5
var n=["pineapple","apple","banana","mango","grapes","orange"]

let pp=document.querySelector("#pp");
let score=document.querySelector("#score");
let sco=0;
let decresco=15;
let load=document.querySelector("#load");
let daddiv=document.querySelector("#daddiv");

let btn2=document.querySelector("#btn2");
let btn=document.querySelector("#btn");
let x=document.querySelectorAll("img");

//adding characters to divs start
var randomcaptcha;
var na;
const appendingvaluetodivs=()=>{
  let m=Math.floor(Math.random()*6);
  randomcaptcha=e2[m]
  na=n[m];
  pp.innerText=na;
  
  load.style.display="revert"
  randarray(e,6)
for(let c=0;c<x.length;c++){

x[c].src=aaa[c]


}

}
   daddiv.style.display="none"
   score.style.display="none"
 appendingvaluetodivs()
//adding characters to divs end


  for(let i=0;i<x.length;i++){
x[i].addEventListener('click',()=>{

  if(singlediv(x[i])==randomcaptcha){

sco+=50;
    score.style.width=`${sco}px`
      appendingvaluetodivs()
     

     
  
      let p=setTimeout(()=>{
        load.style.display="none"
        score.style.display="revert"
        daddiv.style.display="revert"
        
    },500)

    let q=setTimeout(()=>{
      load.style.display="revert"
       score.style.display="none"
       daddiv.style.display="none"
       
    },2000)
 


      let pb=setTimeout(()=>{
       pp.style.display="none"
       
    },50)

    let qa=setTimeout(()=>{
      pp.style.display="block"
     
    },2000)
  }

 else if(singlediv(x[i])!=randomcaptcha){
decresco-=5;


  }
  

if(decresco<10) {
    load.style.pointerEvents="none"
    load.style.opacity="0.2"

  }
if(sco===200){
 load.style.pointerEvents="none"
    load.style.opacity="0.2"
window.location = "https://atanurag.github.io/projects-re/";
}
})


}


function singlediv(g){
  return g.src;
}



//console.log(d.querySelectorAll("#div1").innerHTML)



/*for(let k=0;k<b.length;k++){

for(let a=1;a<b.length;a++){

  if(b[k]!=b[a]){
    continue;

    

  }
 
}
 
}
*/



  var labels = [
    '2022-09-01',
    '2022-09-02',
    '2022-09-03',
    '2022-09-04',
    '2022-09-05',
    '2022-09-06',
  ];

  const data = {
    labels: labels,
    datasets: [{
      label: 'My First dataset',
      backgroundColor: 'rgb(255, 99, 132)',
      borderColor: 'rgb(255, 99, 132)',
      data: [1, 2, 3, 4, 5, 6, 7],
    }]
  };

  const config = {
    type: 'line',
    data: data,
    options: {}
  };

const myChart = new Chart(
    document.getElementById('myChart'),
    config
  );



const fil=()=>{
  var la=[...labels];//copy of labels
  var la1=[...data.datasets[0].data];//copy of data l.h.s
let inp1=document.getElementById("cal1");
let inp2=document.getElementById("cal2");
la.indexOf(inp1.value)
console.log(labels.indexOf(inp1.value),la1)


let filterdate=la.slice(labels.indexOf(inp1.value),labels.indexOf(inp2.value)+1)

let lhsdata=la1.slice(labels.indexOf(inp1.value),labels.indexOf(inp2.value)+1)

myChart.config.data.labels=filterdate



myChart.config.data.datasets[0].data=lhsdata


myChart.update();

console.log(inp1.value.slice(0,4))


}



const aws=async()=>{
console.log(334)

let ede = await fetch("https://www.breakingbadapi.com/api/characters") .then(response => response.json())
  .then((response) =>{ console.log(response)})


console.log(ede)
}

aws()
 console.log(545)

let tryp=new Promise(function(res,rej) {
if(false){
  res();
}
else{
  rej();
}
}) 
tryp.then(()=>{
  console.log("resolve")
}).catch(()=>{
  console.log("reject")
});

//1234567890
//5v5hdsfure

let zx=[1,2,3];
let zxx=`{"1":"one","2":"two"}`;


let aq=JSON.parse(zxx,(key,value)=>{
if(typeof value === "string"){
  return value.toUpperCase();
}
return value;


})


let vvv={
h:function (...i) {
  var c=i
  
 return  c.map((e)=>{

  return e;
  });
  
},
t:22

}

console.log(vvv.h([8,8,5]))
console.log(JSON.stringify(zx),aq)




const ee=(ty)=>{
return ty!=1;

}
let as=[1,2,3,4];

console.log(as.filter((e)=>{
return ee(e);
}))



let switctrial=7;
switch  (switctrial){

case 7:
 alerthello();
break;

case 4:
 alertby();

default :



}

function alerthello() {
console.log("switchcases")}


const fuc=(m)=>{

return 4*m

}

function fuc2(iu) {

 return Object.values(iu).map(r=>r+fuc(6));
 

 

 
}
let cddc={

  oi:4,
 ok:4,
}

console.log(fuc2(cddc));

let ar=[
{
  id:1,
  ja:"333",
  d:["hello","hii"],
  comm:"hellodear",
  isadmi:true
}
,{
  id:2,
  ja:"333",
  d:["hello","hii"]
  ,
  comm:"dear",
  isadmi:false
},{
  id:3,
  ja:"333",
  d:["hello","hii"],
  comm:"my",
  isadmi:true
}

]


const rem=(a)=>{
  let aa=a.filter((e)=>{
    return e.isadmi==true;

  })

  aa.forEach((e)=>{
    return e.d.push("hellowedder")
  })

return aa;
}

console.log(rem(ar));

let l=[1,4,1,4,8]

const tim=(l)=>{
 setTimeout(()=>{ 
console.log(l)
},5000)

}


  let a=[1,2,[3,4,7,[5,8]]];
  let c=[...a[2]]
  let xc=a.slice(0,2);//1st
  console.log(a,a.slice(0,2))
  let r=a[2]
  let v=r.slice(0,3);//2nd
  let fd=r[3]//3rd
console.log(v,r[3])//3rd
console.log([...xc,...v,...fd])
   </script>
  
  </body>
</html>
