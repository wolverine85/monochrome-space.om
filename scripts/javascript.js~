function log(msg) {
    setTimeout(function() {
        throw new Error(msg);
    }, 0);
}
function rotationImg()
{
	var img1 = new Array('#one','#two','#tree', "#four",'#five','#six');
	while(i < img.length)
	{
		$(img[i]).css({'left':+10+'px'});
		i++;
	}
	
}

//alert(screen.availHeight);
$(document).ready(function(){
	document.getElementById("int_body").style.height = (screen.availHeight - document.getElementById("logo").style.height-400)+'px';
//alert(window.innerHeight);	
var _img = new Array('#one','#two','#tree', "#four",'#five','#six');
randImgPos(_img);

randNums = randNumbers();
//alert(randNums);
for (i=0;i<_img.length;i++)
{
	rotate(_img[i]);
	fallingNav(_img[i],randNums[i][0],randNums[i][1]);
}




/////////////////////////////////---------------Test SECTION
	function randNumbers()
	{	
		var numRandNum = new Array();
		var beginPre = 7;
		for(i=0;i<=5;i++)
		{
			numRandNum[i] = new Array();
			numRandNum[i][0] =beginPre+(Math.floor(Math.random())*5 * (Math.floor(Math.random()*2 -1)));
			numRandNum[i][1] = 40-parseInt(Math.random()*25 * (Math.floor(Math.random()*2 -1)));
			beginPre+=10;
		}
		//numRandNum[7][0]=70;
		return numRandNum;
	}
		
	
//var array= new Array('30','35','40','45','50','55','60','65','70');
//array=randNumbers(array);

//alert(array);
//////////////////////////////----------------------------------------END SECTION




mouseHover('img.navImg');


});
	function randImgPos(array)
	{
		for(i=0;i<array.length;i++)
		{ 
		$(array[i]).css({'top':(Math.floor(Math.random()*$('#int_body').height())),'left': (Math.floor(Math.random()*$('#int_body').width()))});
		}
	}

	function fallingNav(obj,randPosX,randPosY)
	{
		
		//var randPosY = 	(Math.floor(Math.random()*($("#int_body").height()-350)			)	+300);
		//var randPosX = (Math.floor(Math.random()* ($("#int_body").width()-300)	+150		));	
		//log("X is: "+randPosX);
		//log("Y is:"+randPosY);
		//log("obj posX:"+$(obj).position().top);
		//log("obj posY:"+$(obj).position().left);
		
		$(obj).animate(
   		{ "left": randPosX +'%',
   	    "top": randPosY +'%'
			 }, 
     		1000, //DURATION
     		"linear", //EASING
     		function()
     		{
     			$(this).css({"transition": "all 2s ease",
			 "-moz-transition":"all 2s ease",
			 "-webkit-transition":" all 2s ease",
			 "-o-transition":"all 2s ease"});
     		}
     	);
		
		//switch(orientation){};
		
	}
	function rotate(obj)
	{
		var rotateIndex = (Math.floor(Math.random()*360))*(Math.random()*2-1); 
		
		$(obj).css({'transform': 'rotate('+rotateIndex+'deg)',
						'-ms-transform': 'rotate('+rotateIndex+'deg)',
						'-webkit-transform':'rotate('+rotateIndex+'deg)',
						'-o-transform': 'rotate('+rotateIndex+'deg)',
						'-moz-transform': 'rotate('+rotateIndex+'deg)'
			});		
	}
	function mouseHover(obj)
	{
		$(obj).hover(
			function()
			{
				$(this).css({'transform':'rotate(0deg) scale(2,2)',
								  '-ms-transform': 'rotate(0deg) scale(2,2)',
							     '-webkit-transform':'rotate(0deg) scale(2,2)',
						        '-o-transform': 'rotate(0deg) scale(2,2)',
						        '-moz-transform': 'rotate(0deg) scale(2,2)',
								  'box-shadow': '10px 10px 5px #000000'
								});
				$('p.category').text(	($(this).attr('alt')));	
				//log('img Starte at:'+ (parseInt($(this).css('left'))+7000));
				
				var centerText =parseInt($(this).offset().left-150);		//$(this).offset().left-100
				//log('text'+centerText);
				//log('img'+$(this).css('margin-right'));
				//log($(this).width());
				$('p.category').css({'text-align':'center','margin-top':($(this).offset().top-400),'margin-left':centerText});								
				$("p.category").stop().fadeIn("fast");
			},
			function()
			{
				var randRot = (Math.floor(Math.random()*360))* (Math.random()*2-1);
				$(this).css({'transform':'rotate('+randRot+'deg)',
								  '-ms-transform': 'rotate('+randRot+'deg)',
							     '-webkit-transform':'rotate('+randRot+'deg)',
						        '-o-transform': 'rotate('+randRot+'deg)',
						        '-moz-transform': 'rotate('+randRot+'deg)',
						        'box-shadow': '2px 2px 1px #666666'								 
								 });
			  $("p.category").fadeOut("fast");
			});
	}
	