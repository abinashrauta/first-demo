# first-demo
this is my first repository
<br>
author -abhi rauta

project random quiz game
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>quiz</title>
    <link rel="stylesheet" href="q.css">
</head>
<body>

    <h1 >quiz competition</h1>

    <div class="jj">
        bye
    </div> 

    <div class="lll">
        hello   
    </div>
    <hr>

<!-- this div for image -->

    
<h2 id="quebox">questions</h2>


<div class="container">
    <div class="quiz">
        
<hr>


        <ul>
            
            
            
            <li>
                <input type="radio" name="abhi" class="hello" id="a" >
            <label for="b" id="option1">option1</label>
            
            </li>
            <li>
                <input type="radio" name="abhi" class="hello" id="b" >
            
            <label for="c" id="option2">optio2</label>                  
            </li>
            <li>
                <input type="radio" name="abhi" class="hello" id="c">
            <label for="d" id="option3">option3</label>
            
            <li>
                <input type="radio" name="abhi" class="hello" id="d" >
            <label for="e" id="option4">option4</label>
            
            

            </li>
            
            </ul>
         

    </div>


    

    
</div >



</div>
<button class="btn" onclick ="submitquize()">submit</button>


    <script src="qu.js"></script>
    
</body>
</html>


<!-- hr for the  straight line -->

<!-- for multiple cursor do multiple at one time alt and click
for........................... javascript...................................................part...................................................
let questions =[{

"que": "what is the css stands for",
 "a":"cascading state style",
"b":"cascading style sheel",
"c" :"cascading style sheet",
"d":"cascading sheet style",
"correct":"c"

},
{
"que": "who is the prime minister of the india",
"a":"mahatma gandhi",
"b":"mahatma gandhi would be wife",
"c":"mahatma gandhi so cold son",
"d":"narendra chai wala modi",

"correct":"d",

},

{
    "que":"who is your inspiration",
    "a":"teacher",

    "b":"ms dhoni",

    "c": "friends",

    "d": "koi nehi yar",

    
    "correct":"c"
},
{
    "que":"what is the html",
    "a":"hyper text mark up language",


    "b":"hypertext markup language",

    "c":"hypertext makeup language",


    "d":"hypertext markoff language",

"correct":"b"


}






]


// //for input access
// let ans = document.querySelectorAll(".hello");
// let h2 = document.querySelector("#bala")

// ///for lable access
// console.log(ans)
// let [questionEle,option_1,option_2,option_3,option_4]= document.querySelectorAll("#option1,#option2,#option3,#option4,#option5");
// console.log(questionEle,option_1,option_2,option_3,option_4)
// // let lable1 = document.querySelector("#option1")
// // let lable2 = document.querySelector("#option2")
// // let lable3 = document.querySelector("#option3")    //aise bhi hoga waise bhi hoga
// // let lable4 = document.querySelector("#option4")
// // console.log(lable1,lable2,lable3,lable4)


// //for buttion access

// let buttion = document.querySelector("button");
// console.log(buttion)


// let currentquiz = 0
// let score = 0;

// //to get the question
// let getdata = ()=>{
//     let{question,ans} = quizquestion[currentquiz];
//     console.log(bala)
//     h2.innerText =question;
// //get tge answar
//     ans.forEach(
//         (curoptions,index)=>(window[`Option${index+1}`].innerText=curoptions)
//     );
// };
// getdata();


// //to find the index 
//     let getselectedoption=()=>{
//        let  answerElement = Array.from(answerElement);
//        return answerElement.findIndex((currentElem)=>currentElem.cheaked);

//     };
   
// buttion.addEventListener("click",()=>{
//     let selectedoptionindex = getselectedoption();
//     console.log(selectedoptionindex)
// })

let index  = 0 ;
right = 0;
wrong = 0;
total = questions.length;
//for question load
let questionbox = document.querySelector("#quebox")
//for option load 
let option = document.querySelectorAll(".hello")

let button = document.querySelector("button")
console.log(button)


let loadquestions = ()=>{
    if(index==total){
        return endquiz();
    }
    reset();
let data = questions[index]//where we get the question quizquestion index se
console.log(data)
questionbox.innerText = `(${index+1})${data.que}`;  // for first one is the increase the index second is the to add the the question and formating the curlybrases and () is the number bracket

//for the options put we have give the input tag class as hello
option[0].nextElementSibling.innerText=data.a
option[1].nextElementSibling.innerText=data.b
option[2].nextElementSibling.innerText=data.c
option[3].nextElementSibling.innerText=data.d

}
const submitquize=()=>{
let data = questions[index]
const ans = getanswar();
if(ans==data.correct){
    right++;
}else{
    wrong++;
}
index++;
loadquestions();
return;
}
const getanswar=()=>{
    let answar;
    option.forEach((input)=>{
        if(input.checked){                  //it means to access the index we give all the lement as id a,b,c,d when user to click ony of these it responese
            answar = input.id
        }
    }
    )
    return answar
}
//for reset because for another question move
const reset =()=>{
    option.forEach((input)=>{
        input.checked=false;
    })
}

//when it reach to the end question and the right and total are of the h2 is the how much right out of that
let endquiz=()=>{
    document.querySelector("body").innerHTML=`
    <h3>your answar is submitted</h3>
    <h2>${right}/${total}are correct</h2>  
    <h1>thank you for playing</h1>

    `
}


loadquestions();
for..........................................................................css..................................................part


body{

    background: -webkit-repeating-radial-gradient( yellow 30% ,black);
/* background:-webkit-repeating-radial-gradient(yellow 50%,blue ); */
}


h1{
    text-align: center;
    background-size: cover;
    color:rgb(72, 0, 255)
    
}
h2{
    color: rgb(43, 0, 255);
}
/* for image center margin auto and width 400px */

.jj{
    height: 200px;
    width: 200px;
    background-color: rgb(255, 0, 43);
    margin-left: auto;
    
    background-image: url('quiz.jpg');      
    background-size: cover;

}
.hello{
    color: red;
}

.quebox{
    color: rgb(149, 0, 255);
}
.btn{
    background-color: rgb(0, 255, 162);
}
.quiz{
    color:white
    
}
