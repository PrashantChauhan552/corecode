<!DOCTYPE html>
<html>
<title>Web Page Design</title>
<head>
<script>
 let TechnicalScore=[];
 let AthleteScore=[];
 
 let ExtraTechnical, ExtraAthelete,totalAthelete,totalTechnical;
function getScore() {
  TechnicalScore.push(1,2,3,4,5,6,7);
  AthleteScore.push(7,45,2,45,44,4,2);
  
  
  getExtraTechnical();
  getExtraAthelete();
//   document.write(""+ExtraAthelete);
  calculate();
  let ASP=(totalAthelete-ExtraAthelete)*30/100
  let TSP=(totalTechnical-ExtraTechnical)*70/100
    document.writeln("Total Athlete Score:"+ASP);
    document.writeln("\n Total Technical Score:"+TSP);
  
  document.writeln("\n Total Score:"+(ASP+TSP));
  
 
}


function getExtraTechnical()
{
     ExtraTechnical=Math.min(...TechnicalScore) + Math.max(...TechnicalScore);
}

function getExtraAthelete()
{
   ExtraAthelete=Math.min(...AthleteScore) + Math.max(...AthleteScore);
}

function calculate()
{
    totalTechnical=0;
    totalAthelete=0;
 for(let i=0;i<TechnicalScore.length;i++)
 {
     totalTechnical=TechnicalScore[i]+totalTechnical;
     totalAthelete=AthleteScore[i]+totalAthelete;
    //  console.log(totalAthelete);
 }
}


getScore();
</script>
</head>
<body>
</body>
</html>
