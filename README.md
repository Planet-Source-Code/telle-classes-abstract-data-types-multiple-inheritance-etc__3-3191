<div align="center">

## Classes, Abstract Data Types, Multiple Inheritance, etc


</div>

### Description

This is basicly some notes i made for Classes, Abstract Data Types, Multiple Inheritance, and things like that
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[telle](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/telle.md)
**Level**          |Intermediate
**User Rating**    |2.6 (13 globes from 5 users)
**Compatibility**  |Microsoft Visual C\+\+
**Category**       |[Classes/ Frameworks/ OOP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/classes-frameworks-oop__3-31.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/telle-classes-abstract-data-types-multiple-inheritance-etc__3-3191/archive/master.zip)





### Source Code

<head><title>Classes</title>
<style>
<!--
 /* Font Definitions */
 @font-face
	{font-family:"MS Mincho";
	panose-1:2 2 6 9 4 2 5 8 3 4;
	mso-font-alt:"\FF2D\FF33 \660E\671D";
	mso-font-charset:128;
	mso-generic-font-family:modern;
	mso-font-pitch:fixed;
	mso-font-signature:-1610612033 1757936891 16 0 131231 0;}
@font-face
	{font-family:Century;
	panose-1:2 4 6 4 5 5 5 2 3 4;
	mso-font-charset:0;
	mso-generic-font-family:roman;
	mso-font-pitch:variable;
	mso-font-signature:647 0 0 0 159 0;}
@font-face
	{font-family:"\@MS Mincho";
	panose-1:2 2 6 9 4 2 5 8 3 4;
	mso-font-charset:128;
	mso-generic-font-family:modern;
	mso-font-pitch:fixed;
	mso-font-signature:-1610612033 1757936891 16 0 131231 0;}
 /* Style Definitions */
 p.MsoNormal, li.MsoNormal, div.MsoNormal
	{mso-style-parent:"";
	margin:0mm;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	mso-pagination:none;
	font-size:10.5pt;
	mso-bidi-font-size:12.0pt;
	font-family:Century;
	mso-fareast-font-family:"MS Mincho";
	mso-bidi-font-family:"Times New Roman";
	mso-font-kerning:1.0pt;}
span.SpellE
	{mso-style-name:"";
	mso-spl-e:yes;}
span.GramE
	{mso-style-name:"";
	mso-gram-e:yes;}
 /* Page Definitions */
 @page
	{mso-page-border-surround-header:no;
	mso-page-border-surround-footer:no;}
@page Section1
	{size:595.3pt 841.9pt;
	margin:99.25pt 30.0mm 30.0mm 30.0mm;
	mso-header-margin:36.0pt;
	mso-footer-margin:36.0pt;
	mso-paper-source:0;
	layout-grid:18.0pt;}
div.Section1
	{page:Section1;}
-->
</style>
<!--[if gte mso 10]>
<style>
 /* Style Definitions */
 table.MsoNormalTable
	{mso-style-name:"Table Normal";
	mso-tstyle-rowband-size:0;
	mso-tstyle-colband-size:0;
	mso-style-noshow:yes;
	mso-style-parent:"";
	mso-padding-alt:0mm 5.4pt 0mm 5.4pt;
	mso-para-margin:0mm;
	mso-para-margin-bottom:.0001pt;
	mso-pagination:widow-orphan;
	font-size:10.0pt;
	font-family:Century;}
</style>
<body lang=JA style='tab-interval:42.0pt;text-justify-trim:punctuation'>
<div class=Section1 style='layout-grid:18.0pt'>
<p class=MsoNormal><b><u><span lang=EN-US>Classes<o:p></o:p></span></u></b></p>
<p class=MsoNormal><span lang=EN-US>With classes, everything is <i>private</i>,
unless specified otherwise (Using the <b>public:</b> statement). When I say ‘<i>private’</i>,
I mean everything declared under <i>private</i> is not seen by the programmer. <i>Public</i>
declarations are seen by the programmer. Now, you should know that every time a
class is created, a new <i>instance</i> is created. Within a class’s block
scope you declare functions/constructor/deconstructor. It is not recommended to
implant the code of functions for the class directly into the class, but by
using the <b>inline</b> keyword. To define a function outside of a class’s
block scope you use this format:</span></p>
<p class=MsoNormal><span lang=EN-US><o:p> </o:p></span></p>
<p class=MsoNormal><i><span lang=EN-US>Class_Name</span></i><b><span
lang=EN-US>::</span></b><i><span lang=EN-US>Function_Name</span></i><span
lang=EN-US>(<b>arguments</b>) { <i>//function code</i> }</span></p>
<p class=MsoNormal><span lang=EN-US><o:p> </o:p></span></p>
<p class=MsoNormal><span lang=EN-US>Now, there may come a time when you want a
variable value to be the same through all the instances of the class, or you
may just want to share the variable value through all the instances (for
example, you might want to have a count of all the instances of a class). In
order to do this, you use the <b>static</b> keyword. The format is as follows:</span></p>
<p class=MsoNormal><span lang=EN-US><o:p> </o:p></span></p>
<p class=MsoNormal><span lang=EN-US>Static Variable_Type Variable_Name;</span></p>
<p class=MsoNormal><span lang=EN-US><o:p> </o:p></span></p>
<p class=MsoNormal><span lang=EN-US>Here is an example that shows the use of a
static variable in a class:</span></p>
<p class=MsoNormal><span lang=EN-US><o:p> </o:p></span></p>
<p class=MsoNormal><i><span lang=EN-US>class STClass<o:p></o:p></span></i></p>
<p class=MsoNormal><i><span lang=EN-US>{<o:p></o:p></span></i></p>
<p class=MsoNormal><i><span lang=EN-US>int x; //private declaration<o:p></o:p></span></i></p>
<p class=MsoNormal><i><span lang=EN-US>int y; //private declaration<o:p></o:p></span></i></p>
<p class=MsoNormal><i><span lang=EN-US>static int count; //static declaration,
private<o:p></o:p></span></i></p>
<p class=MsoNormal><i><span lang=EN-US>inline counts()<o:p></o:p></span></i></p>
<p class=MsoNormal><i><span lang=EN-US>{<o:p></o:p></span></i></p>
<p class=MsoNormal><i><span lang=EN-US>count++;<o:p></o:p></span></i></p>
<p class=MsoNormal><i><span lang=EN-US>}<o:p></o:p></span></i></p>
<p class=MsoNormal><span lang=EN-US><o:p> </o:p></span></p>
<p class=MsoNormal><span lang=EN-US>STClass St1;</span></p>
<p class=MsoNormal><span lang=EN-US>STClass St2;</span></p>
<p class=MsoNormal><span lang=EN-US><o:p> </o:p></span></p>
<p class=MsoNormal><span lang=EN-US>Basically, count is going to equal 2.</span></p>
<p class=MsoNormal><span lang=EN-US><o:p> </o:p></span></p>
<p class=MsoNormal><b><span lang=EN-US>Function Polymorphism </span></b><span
lang=EN-US>in Classes</span></p>
<p class=MsoNormal><span lang=EN-US>Polymorphism pretty much means many forms,
and thus, function polymorphism means many forms of a function.</span></p>
<p class=MsoNormal><span lang=EN-US>Function Polymorphism is there pretty much
for the user to decide which function they want to use. Now, you should know,
this really isn’t different from Function Overloading, which will be explained
later on.</span></p>
<p class=MsoNormal><span lang=EN-US><o:p> </o:p></span></p>
<p class=MsoNormal><b><span lang=EN-US>Abstract Data Type<o:p></o:p></span></b></p>
<p class=MsoNormal><span lang=EN-US>Abstract Data Type’s require a pure
function, or a NULL function. A format for an ADT is as follows:</span></p>
<p class=MsoNormal><span lang=EN-US>vital void Function Name(arguments) = 0;</span></p>
<p class=MsoNormal><span lang=EN-US>The format can vary.</span></p>
<p class=MsoNormal><span lang=EN-US><o:p> </o:p></span></p>
<p class=MsoNormal><b><span lang=EN-US>Multiple <span class=GramE>Inheritance</span><o:p></o:p></span></b></p>
<p class=MsoNormal><span lang=EN-US>Multiple <span class=GramE>Inheritance</span>
is the ability to transform an array of classes into one. </span></p>
<p class=MsoNormal><span lang=EN-US>Here is an example on Multiple Inheritance:</span></p>
<p class=MsoNormal><span lang=EN-US><o:p> </o:p></span></p>
<p class=MsoNormal><span lang=EN-US>Class This</span></p>
<p class=MsoNormal><span lang=EN-US>{</span></p>
<p class=MsoNormal><span lang=EN-US>int x;</span></p>
<p class=MsoNormal><span lang=EN-US>int y;</span></p>
<p class=MsoNormal><span lang=EN-US>}</span></p>
<p class=MsoNormal><span lang=EN-US><o:p> </o:p></span></p>
<p class=MsoNormal><span lang=EN-US>Class That</span></p>
<p class=MsoNormal><span lang=EN-US>{</span></p>
<p class=MsoNormal><span lang=EN-US>int z;</span></p>
<p class=MsoNormal><span lang=EN-US>}</span></p>
<p class=MsoNormal><span lang=EN-US><o:p> </o:p></span></p>
<p class=MsoNormal><span lang=EN-US>Class <span class=SpellE>ThisNThat</span> :
public This, public That</span></p>
<p class=MsoNormal><span lang=EN-US>{</span></p>
<p class=MsoNormal><span lang=EN-US>x = 100;</span></p>
<p class=MsoNormal><span lang=EN-US>y = 200;</span></p>
<p class=MsoNormal><span lang=EN-US>z = x + y;</span></p>
<p class=MsoNormal><span lang=EN-US>}<o:p></o:p></span></p>
</div>
</body>
</html>

