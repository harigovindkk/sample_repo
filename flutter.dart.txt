import 'dart:io';
class Screening
{
  var field = new List();
  var pid = new List(); 
  var time1 = new List(); 
  var time2 = new List(); 
  var timereqd  = new List(); 
  var fieldreqd = new List(); String f;int lm,ta,tb,ra,rb;
  
   void main() 
{
  for(int i=0;i<10;i++)
  {
    addStacks();
  int select=setMentorOrLearner();
  if(select==1)
  setAvailableTime();
  else
  getMentor();
  }
  
}
  addStacks()
  {
    print('Enter your field of interest/expertise');
   f = stdin.readLineSync();
    field.add(f);
  }
   setMentorOrLearner()
  {
    print('Are you a mentor or learner? If mentor, enter 1 else 2 ');
    lm= (int.parse(stdin.readLineSync()));
    pid.add(lm);
    return lm;
  }
   setAvailableTime()
  {
   if(lm==1)
   {
     print('Enter your available time (starting time in 24hr format)');
     ta=int.parse(stdin.readLineSync());
     time1.add(ta);
      print('Enter your available time (ending time in 24hr format)');
     tb= int.parse(stdin.readLineSync());
     time2.add(tb);
   }
  }
  getMentor()
  { 
    print('Enter your required starting time');
    ra=int.parse(stdin.readLineSync());
    timereqd.add(ra);
    print('Enter your required ending time');
    rb=int.parse(stdin.readLineSync());
    timereqd.add(rb);
    print('enter your required field');
    fieldreqd.add(stdin.readLineSync());
    
  }
}