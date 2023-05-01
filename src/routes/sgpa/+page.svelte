<script>
    var credit1=0;
    var credit2=0;
    var credit3=0;
    var credit4=0;
    var credit5=0;
    var credit6=0;
    var credit7=0;
    var credit8=0;
    var credit9=0;
    var credit10=0;
    var gpa1=0;
    var gpa2=0;
    var gpa3=0;
    var gpa4=0;
    var gpa5=0;
    var gpa6=0;
    var gpa7=0;
    var gpa8=0;
    var gpa9=0;
    var gpa10=0;

    var totalCredit=0;
    var totalgpa=0;
    
    function addgpa1(){
        var grade =document.getElementById('grade1').value;
        credit1 = document.getElementById('credit1').value;
        gpa1=parseFloat(grade)*parseFloat(credit1);
        document.getElementById('gpa1').value=gpa1;
    }
    function addgpa2(){
        var grade =document.getElementById('grade2').value;
        credit2 = document.getElementById('credit2').value;
        gpa2=parseFloat(grade)*parseFloat(credit2);
        document.getElementById('gpa2').value=gpa2;
    }
    function addgpa3(){
        var grade =document.getElementById('grade3').value;
        credit3 = document.getElementById('credit3').value;
        gpa3=parseFloat(grade)*parseFloat(credit3);
        document.getElementById('gpa3').value=gpa3;
    }
    function addgpa4(){
        var grade =document.getElementById('grade4').value;
        credit4 = document.getElementById('credit4').value;
        gpa4=parseFloat(grade)*parseFloat(credit4);
        document.getElementById('gpa4').value=gpa4;
    }
    function addgpa5(){
        var grade =document.getElementById('grade5').value;
        credit5 = document.getElementById('credit5').value;
        gpa5=parseFloat(grade)*parseFloat(credit5);
        document.getElementById('gpa5').value=gpa5;
    }
    function addgpa6(){
        var grade =document.getElementById('grade6').value;
        credit6 = document.getElementById('credit6').value;
        gpa6=parseFloat(grade)*parseFloat(credit6);
        document.getElementById('gpa6').value=gpa6;
    }
    function addgpa7(){
        var grade =document.getElementById('grade7').value;
        credit7 = document.getElementById('credit7').value;
        gpa7=parseFloat(grade)*parseFloat(credit7);
        document.getElementById('gpa7').value=gpa7;
    }
    function addgpa8(){
        var grade =document.getElementById('grade8').value;
        credit8 = document.getElementById('credit8').value;
        gpa8=parseFloat(grade)*parseFloat(credit8);
        document.getElementById('gpa8').value=gpa8;
    }
    function addgpa9(){
        var grade =document.getElementById('grade9').value;
        credit9 = document.getElementById('credit9').value;
        gpa9=parseFloat(grade)*parseFloat(credit9);
        document.getElementById('gpa9').value=gpa9;
    }
    function addgpa10(){
        var grade =document.getElementById('grade10').value;
        credit10 = document.getElementById('credit10').value;
        gpa10=parseFloat(grade)*parseFloat(credit10);
        document.getElementById('gpa10').value=gpa10;
    }
    function calculatesgpa(){
        var result = 0;
        totalCredit = parseFloat(credit1)+parseFloat(credit2)+parseFloat(credit3)+parseFloat(credit4)+parseFloat(credit5)+parseFloat(credit6)+parseFloat(credit7)+parseFloat(credit8)+parseFloat(credit9)+parseFloat(credit10);
        totalgpa = parseFloat(gpa1)+parseFloat(gpa2)+parseFloat(gpa3)+parseFloat(gpa4)+parseFloat(gpa5)+parseFloat(gpa6)+parseFloat(gpa7)+parseFloat(gpa8)+parseFloat(gpa9)+parseFloat(gpa10);
        alert("=>Total GPA: "+totalgpa+"  =>Total Credit:"+totalCredit)
        result = parseFloat(totalgpa)/parseFloat(totalCredit);
        document.getElementById('sgpa-box').value = "Your SGPA : "+result;
    }

</script>

<svelte:head>
	<title>Calculate SGPA</title>
</svelte:head>

<div class="text-column">
    <h1 class="cgpa-head">Find your Semster GPA</h1>
    <p class="cgpa-desc">
        <strong>What is SGPA ?</strong><br>
    	SGPA is an acronym for <em>Semster Grade Point Average</em>.It is a score awarded to students based on how well they have fared in their course work at the end of each semester. SGPA is calculated as the weighted average of the grade points earned by a student in a semester across all subjects<br>
        <strong>How to Use ?</strong><br>
        1. Enter your <b>subject,mark and their credit point</b><br>
        2. Click on the <b>+</b> icon,after you can see <b>GPA</b> corresponding Subject<br>
        3. After all subject entered and got their gpa, Click on Calculate to find GPA 
        <strong>Preffered Device : Computer OR Smartphone</strong>
    </p>
    
    <div class="form-cont">
            <div class="all-field">
                <p class="field">Subject</p>
                <p class="field">Grade</p>
                <p class="field">Credit</p>
                <p class="field" style="margin-left: 6vh;">GPA</p>
            </div>
            <div class="markfield">
                <div class="Tablemarks">
                    <input type="text" name="sub1" id="sub1" placeholder="Subject 1">
                    <div class="select-cg">
                        <select name="grade" id="grade1">
                            <option selected="selected" disabled="disabled">Select Grade</option>
                            <optgroup label="Passed">
                                <option value="10">S</option>
                                <option value="9">A</option>
                                <option value="8">B</option>
                                <option value="7">C</option>
                                <option value="6">D</option>
                                <option value="5">E</option>
                            </optgroup>
                            <optgroup label="Failed">
                                <option value="0">F</option>
                            </optgroup>
                        </select> 
                    </div>
                    <div class="select-cg">
                        <select name="credit" id="credit1">
                            <option selected="selected" disabled="disabled">Select Credit</option>
                            <option value="0">0</option>
                            <option value="1">1</option>
                            <option value="1.5">1.5</option>
                            <option value="2">2</option>
                            <option value="2.5">2.5</option>
                            <option value="3">3</option>
                            <option value="3.5">3.5</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                        </select>
                    </div>
                    <button class="plus" on:click={addgpa1}>+</button>
                    <input type="text" name="gpa1" id="gpa1" placeholder="GPA" disabled>
                    <p class="gpa1"></p>
                </div>

                <div class="Tablemarks">
                    <input type="text" name="sub1" id="sub2" placeholder="Subject 2">
                    <div class="select-cg">
                        <select name="grade" id="grade2">
                            <option selected="selected" disabled="disabled">Select Grade</option>
                            <optgroup label="Passed">
                                <option value="10">S</option>
                                <option value="9">A</option>
                                <option value="8">B</option>
                                <option value="7">C</option>
                                <option value="6">D</option>
                                <option value="5">E</option>
                            </optgroup>
                            <optgroup label="Failed">
                                <option value="0">F</option>
                            </optgroup>
                        </select> 
                    </div>
                    <div class="select-cg">
                        <select name="credit" id="credit2">
                            <option selected="selected" disabled="disabled">Select Credit</option>
                            <option value="0">0</option>
                            <option value="1">1</option>
                            <option value="1.5">1.5</option>
                            <option value="2">2</option>
                            <option value="2.5">2.5</option>
                            <option value="3">3</option>
                            <option value="3.5">3.5</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                        </select>
                    </div>
                    <button class="plus" on:click={addgpa2}>+</button>
                    <input type="text" name="gpa2" id="gpa2" placeholder="GPA" disabled>
                    <p class="gpa1"></p>
                </div>
    
                 <div class="Tablemarks">
                    <input type="text" name="sub1" id="sub3" placeholder="Subject 3">
                    <div class="select-cg">
                        <select name="grade" id="grade3">
                            <option selected="selected" disabled="disabled">Select Grade</option>
                            <optgroup label="Passed">
                                <option value="10">S</option>
                                <option value="9">A</option>
                                <option value="8">B</option>
                                <option value="7">C</option>
                                <option value="6">D</option>
                                <option value="5">E</option>
                            </optgroup>
                            <optgroup label="Failed">
                                <option value="0">F</option>
                            </optgroup>
                        </select> 
                    </div>
                    <div class="select-cg">
                        <select name="credit" id="credit3">
                            <option selected="selected" disabled="disabled">Select Credit</option>
                            <option value="0">0</option>
                            <option value="1">1</option>
                            <option value="1.5">1.5</option>
                            <option value="2">2</option>
                            <option value="2.5">2.5</option>
                            <option value="3">3</option>
                            <option value="3.5">3.5</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                        </select>
                    </div>
                    <button class="plus" on:click={addgpa3}>+</button>
                    <input type="text" name="gpa3" id="gpa3" placeholder="GPA" disabled>
                </div>
    
                <div class="Tablemarks">
                    <input type="text" name="sub1" id="sub4" placeholder="Subject 4">
                    <div class="select-cg">
                        <select name="grade" id="grade4">
                               <option selected="selected" disabled="disabled">Select Grade</option>
                            <optgroup label="Passed">
                                <option value="10">S</option>
                                <option value="9">A</option>
                                <option value="8">B</option>
                                <option value="7">C</option>
                                <option value="6">D</option>
                                <option value="5">E</option>
                            </optgroup>
                            <optgroup label="Failed">
                                <option value="0">F</option>
                            </optgroup>
                        </select> 
                    </div>
                    <div class="select-cg">
                        <select name="credit" id="credit4">
                            <option selected="selected" disabled="disabled">Select Credit</option>
                            <option value="0">0</option>
                            <option value="1">1</option>
                            <option value="1.5">1.5</option>
                            <option value="2">2</option>
                            <option value="2.5">2.5</option>
                            <option value="3">3</option>
                            <option value="3.5">3.5</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                        </select>
                    </div>
                    <button class="plus" on:click={addgpa4}>+</button>
                    <input type="text" name="gpa4" id="gpa4" placeholder="GPA" disabled>
                </div>
    
                <div class="Tablemarks">
                    <input type="text" name="sub1" id="sub5" placeholder="Subject 5">
                    <div class="select-cg">
                        <select name="grade" id="grade5">
                            <option selected="selected" disabled="disabled">Select Grade</option>
                            <optgroup label="Passed">
                                <option value="10">S</option>
                                <option value="9">A</option>
                                <option value="8">B</option>
                                <option value="7">C</option>
                                <option value="6">D</option>
                                <option value="5">E</option>
                            </optgroup>
                            <optgroup label="Failed">
                                <option value="0">F</option>
                            </optgroup>
                        </select> 
                    </div>
                    <div class="select-cg">
                        <select name="credit" id="credit5">
                            <option selected="selected" disabled="disabled">Select Credit</option>
                            <option value="0">0</option>
                            <option value="1">1</option>
                            <option value="1.5">1.5</option>
                            <option value="2">2</option>
                            <option value="2.5">2.5</option>
                            <option value="3">3</option>
                            <option value="3.5">3.5</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                        </select>
                    </div>
                    <button class="plus" on:click={addgpa5}>+</button>
                    <input type="text" name="gpa5" id="gpa5" placeholder="GPA" disabled>
                </div>
    
                <div class="Tablemarks">
                    <input type="text" name="sub1" id="sub6" placeholder="Subject 6">
                    <div class="select-cg">
                        <select name="grade" id="grade6">
                            <option selected="selected" disabled="disabled">Select Grade</option>
                            <optgroup label="Passed">
                                <option value="10">S</option>
                                <option value="9">A</option>
                                <option value="8">B</option>
                                <option value="7">C</option>
                                <option value="6">D</option>
                                <option value="5">E</option>
                            </optgroup>
                            <optgroup label="Failed">
                                <option value="0">F</option>
                            </optgroup>
                        </select> 
                    </div>
                    <div class="select-cg">
                        <select name="credit" id="credit6">
                            <option selected="selected" disabled="disabled">Select Credit</option>
                            <option value="0">0</option>
                            <option value="1">1</option>
                            <option value="1.5">1.5</option>
                            <option value="2">2</option>
                            <option value="2.5">2.5</option>
                            <option value="3">3</option>
                            <option value="3.5">3.5</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                        </select>
                    </div>
                    <button class="plus" on:click={addgpa6}>+</button>
                    <input type="text" name="gpa6" id="gpa6" placeholder="GPA" disabled>
                </div>
    
                <div class="Tablemarks">
                    <input type="text" name="sub1" id="sub7" placeholder="Subject 7">
                    <div class="select-cg">
                        <select name="grade" id="grade7">
                            <option selected="selected" disabled="disabled">Select Grade</option>
                            <optgroup label="Passed">
                                <option value="10">S</option>
                                <option value="9">A</option>
                                <option value="8">B</option>
                                <option value="7">C</option>
                                <option value="6">D</option>
                                <option value="5">E</option>
                            </optgroup>
                            <optgroup label="Failed">
                                <option value="0">F</option>
                            </optgroup>
                        </select> 
                    </div>
                    <div class="select-cg">
                        <select name="credit" id="credit7">
                            <option selected="selected" disabled="disabled">Select Credit</option>
                            <option value="0">0</option>
                            <option value="1">1</option>
                            <option value="1.5">1.5</option>
                            <option value="2">2</option>
                            <option value="2.5">2.5</option>
                            <option value="3">3</option>
                            <option value="3.5">3.5</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                        </select>
                    </div>
                    <button class="plus" on:click={addgpa7}>+</button>
                    <input type="text" name="gpa7" id="gpa7" placeholder="GPA" disabled>
                </div>
    
                <div class="Tablemarks">
                    <input type="text" name="sub1" id="sub8" placeholder="Subject 8">
                    <div class="select-cg">
                        <select name="grade" id="grade8">
                            <option selected="selected" disabled="disabled">Select Grade</option>
                            <optgroup label="Passed">
                                <option value="10">S</option>
                                <option value="9">A</option>
                                <option value="8">B</option>
                                <option value="7">C</option>
                                <option value="6">D</option>
                                <option value="5">E</option>
                            </optgroup>
                            <optgroup label="Failed">
                                <option value="0">F</option>
                            </optgroup>
                        </select> 
                    </div>
                    <div class="select-cg">
                        <select name="credit" id="credit8">
                            <option selected="selected" disabled="disabled">Select Credit</option>
                            <option value="0">0</option>
                            <option value="1">1</option>
                            <option value="1.5">1.5</option>
                            <option value="2">2</option>
                            <option value="2.5">2.5</option>
                            <option value="3">3</option>
                            <option value="3.5">3.5</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                        </select>
                    </div>
                    <button class="plus" on:click={addgpa8}>+</button>
                    <input type="text" name="gpa8" id="gpa8" placeholder="GPA" disabled>
                </div>
    
                <div class="Tablemarks">
                    <input type="text" name="sub1" id="sub9" placeholder="Subject 9">
                    <div class="select-cg">
                        <select name="grade" id="grade9">
                            <option selected="selected" disabled="disabled">Select Grade</option>
                            <optgroup label="Passed">
                                <option value="10">S</option>
                                <option value="9">A</option>
                                <option value="8">B</option>
                                <option value="7">C</option>
                                <option value="6">D</option>
                                <option value="5">E</option>
                            </optgroup>
                            <optgroup label="Failed">
                                <option value="0">F</option>
                            </optgroup>
                        </select> 
                    </div>
                    <div class="select-cg">
                        <select name="credit" id="credit9">
                            <option selected="selected" disabled="disabled">Select Credit</option>
                            <option value="0">0</option>
                            <option value="1">1</option>
                            <option value="1.5">1.5</option>
                            <option value="2">2</option>
                            <option value="2.5">2.5</option>
                            <option value="3">3</option>
                            <option value="3.5">3.5</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                        </select>
                    </div>
                    <button class="plus" on:click={addgpa9}>+</button>
                    <input type="text" name="gpa9" id="gpa9" placeholder="GPA" disabled>
                </div>
    
                <div class="Tablemarks">
                    <input type="text" name="sub1" id="sub10" placeholder="Subject 10">
                    <div class="select-cg">
                        <select name="grade" id="grade10">
                            <option selected="selected" disabled="disabled">Select Grade</option>
                            <optgroup label="Passed">
                                <option value="10">S</option>
                                <option value="9">A</option>
                                <option value="8">B</option>
                                <option value="7">C</option>
                                <option value="6">D</option>
                                <option value="5">E</option>
                            </optgroup>
                            <optgroup label="Failed">
                                <option value="0">F</option>
                            </optgroup>
                        </select> 
                    </div>
                    <div class="select-cg">
                        <select name="credit" id="credit10">
                            <option selected="selected" disabled="disabled">Select Credit</option>
                            <option value="0">0</option>
                            <option value="1">1</option>
                            <option value="1.5">1.5</option>
                            <option value="2">2</option>
                            <option value="2.5">2.5</option>
                            <option value="3">3</option>
                            <option value="3.5">3.5</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                        </select>
                    </div>
                    <button class="plus" on:click={addgpa10}>+</button>
                    <input type="text" name="gpa10" id="gpa10" placeholder="GPA" disabled>
                </div>    
                
            </div>

            <br><br>
            <div class="res-sgpa">
                <button on:click={calculatesgpa} class="cal-style">Calculate</button>
            </div>
            <br><br>
            <div class="res-sgpa">
                <input type="text" name="sgpa-box" id="sgpa-box" value="Your SGPA " disabled>
            </div>

    </div>

</div>

<style>
    .cgpa-head{
        display: flexbox;
        justify-content: left;
        align-items: left;
        flex-direction: column;

        margin-right: 40%;
        font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        margin-bottom: 0px;
    }
    .cgpa-desc{
        margin-top: 4px;
        font-size: 12px;
        margin-left: 9%;
    }
    .form-cont{
        background-color: rgba(255, 123, 0, 0.288);
        padding: 5%;
        border-radius: 16px;
    }

    input[type="text"]::placeholder{
        color: white;
    }

    .field{
        display: inline-block;
        width: 16vh;
        padding: 10px;
        box-shadow: 0 5px 25px rgba(48, 43, 43, 0.3);
        text-align: center;
        margin-left: 0.4vh;
    }

    input[type="text"]{
        border-radius: 7px;
        background-color: #f8720b;
        color: white;
        padding: 10px;
        width: 16vh;
        border: none;
        margin: 5px;
        margin-left: 0px;
        box-shadow: 0 5px 25px rgba(0, 0, 0, 0.3);
    }
    input[type="text"]::placeholder{
        color: white;

    }
    .select-cg {
      display: inline-block;
    }

    input[type="text"],div select{
        margin-top: 10px;
        margin-bottom: 10px;
    }

    select{
      margin: 5px;
      text-align: center;
      border-radius: 7px;
      background-color: #f8360b;
      color: white;
      padding: 10px;
      border: none;
      font-size: 16px;
      box-shadow: 0 5px 25px rgba(0, 0, 0, 0.3);
      -webkit-appearance: button;
      appearance: button;
      outline: none;
    }

    .select-cg::before {
        text-align: center;
        font-size: 28px;
        line-height: 45px;
        color: rgba(255, 255, 255, 0.5);
        background-color: rgba(255, 255, 255, 0.1);
        pointer-events: none;
    }

    .select-cg:hover::before {
        color: rgba(255, 255, 255, 0.6);
        background-color: rgba(255, 255, 255, 0.2);
    }

    .select-cg select option {
        padding: 30px;
    }
    .plus{
        border-radius: 7px;
        background-color: #b95000;
        font-size: 15px;
        color: white;
        padding: 0px;
        height: 5vh;
        width: 5vh;
        border: none;
        margin-right: 5px;
        box-shadow: 0 5px 25px rgba(0, 0, 0, 0.3);
    }
    .plus:hover{
        border-radius: 0px;
        background-color: #ecec40;
        transition: 1s;
    }
    .plus:active{
        border-radius: 0px;
        background-color: #000000;
    }
    .cal-style{
        border-radius: 7px;
        background: linear-gradient(10deg,rgb(83, 39, 3),black);
        font-size: 25px;
        font-weight: 300;
        font-family:Verdana, Geneva, Tahoma, sans-serif;
        color: white;
        padding: 10px;
        padding-left: 40px;
        padding-right: 40px;
        text-align: center;
        border: none;
        margin-right: 5px;
        box-shadow: 0px 5px 15px 5px rgba(0, 0, 0, 0.3);
    }
    .cal-style:hover{
        outline: 3px solid black;
        outline-offset: 10px;
        transition: 0.3s;
    }
    .cal-style:active{
        background-color: rgba(0,0,0,1);
        border: 1px solid rgb(55, 255, 0);
        transition: 0.1s;
    }
    .res-sgpa{
        margin: 0 auto;
        margin-left: auto;
        margin-right: auto;
        text-align:center;
    }
    #sgpa-box{
        color: black;
        font-size: 50px;
        width: 90%;
        padding: 20px;
        background-color: whitesmoke;
        justify-items: center;
        text-align: center;
    }

    @media screen and (max-width: 600px)
    {
        .cgpa-head{
            margin-right: 0;
            color:black;
            margin-bottom: 10px;
        }
        .field{
            visibility: hidden;
            padding: 0px;
            margin: 0px;
        }
        .Tablemarks{
            margin-left: 0px;
            margin-bottom: 10px;
        }
        .markfield,select{
            margin-left: 0px;
        }
        .select-cg select option {
            padding: 0px;
            margin: 0px;
        }
        .select-cg::before{
            padding: 0px;
            margin: 0px;
        }
        #sgpa-box{
            font-size: 20px;
            width: 80%;
            padding: 20px;
            background-color: whitesmoke;
            justify-items: center;
            text-align: center;
        }
    }
</style>