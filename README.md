# MyFirstApp
Android project from codelabs
https://codelabs.developers.google.com/codelabs/build-your-first-android-app/index.html?index=..%2F..index#0

The project listed on the site is great but falls apart at the end. 
There are issues with Task 9 - Step 6 and Task 9 - Step 7.

I was able to resolve the issues and get the app to work as intended. This code is the completed application.
Disclaimer: I am a beginner and there is no claim made that the methods I used are good practice, efficient or even right (other than the fact that it works).
Experts feel free to offer me feedback on how I could have done this better. Fellow novices feel free to ask questions. 

Here in the readme I will offer some breadcrumbs for those who are trying to do it themselves:

Task 9 - Step 6
---------------------------------------------------
The line:
FirstFragmentDirections.ActionFirstFragmentToSecondFragment action =
       FirstFragmentDirections.
               actionFirstFragmentToSecondFragment(currentCount);

Won't work without some adjusments to gradle. 
I was able to find a clue in Issue Report #19 on github: 
https://github.com/google-developer-training/first-android-app/issues/19
The gentleman who brought up this issue pointed me in the direction of the android developer pages which helps to explain the solution:
https://developer.android.com/guide/navigation/navigation-pass-data#Safe-args

5. In SecondFragment.java, change myArg from a String to an Integer.

But that line doesn't exist. Just add the one found in the tutorial.

Task 9 - Step 7
-----------------------------------------------------
After following the directions to the best of my abilty but there were some things missing in SecondFragment.java.
It mentions entering a line under the code that sets the header text - but I couldn't find any code that sets the header text. 
You have to do this yourself to get the App working as described in the tutorial. What I did was look at how the TextView showCountTextView
was updated in the countMe function in FirstFragment.java and used that as a clue on what I needed to do to create/update the textview_header.
I used this StackOverflow question to remind me how to update the placeholder %d in the String:
https://stackoverflow.com/questions/33164886/android-textview-do-not-concatenate-text-displayed-with-settext
