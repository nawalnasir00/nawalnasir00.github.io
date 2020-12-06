---
layout: default
---
Hi, my name is #Nawal Nasir

Welcome to my page where I discuss some of my past experiences and projects!


## About


I am currently a third year student at Brooklyn College. I am working towards a Bachelors of Science degree, majoring in Computer Science. I am the youngest of three children, all of whom are in the medical field. I have decided to pursue Computer Science because I enjoy programming and seeing how everything works together. I am also interested in Data Science because I think that using data and numbers to find solutions is very fun! My future goal is to work at a non-profit organization and help make a difference.  



## Experiences
**Blackstone**

My internship at Blackstone was amazing. I was able to create a Slack slash command with my group to compliment colleagues. I also met with many professionals of various fields and learned about their careers. I was able to learn about the business aspect of a company. 

**WebMD**

My internship at WebMD was very eye-opening. It was the first time I was able to see how medical and computer science worked together. I was able to see firsthand what a software engineer does which has definitely played a part in choosing what I want to pursue.


## Projects
**Life Simulator**

import java.util.Scanner;
public class LifeSimulator {
	public static void main(String[] args) {


        Scanner s = new Scanner(System.in);
        
        final String BUSINESS_MAN = "a businessman/woman";
        final String ENGINEER = "a engineer";
        final String ARTIST = "an artist";
        final String HELPING_PROFESSION = "a helping profession";
        final String UNEMPLOYED = "unemployed";
        
        final double CHANCE_OF_BUSINESS = 0.30;
        final double CHANCE_OF_ENGINEER = 0.05;
        final double CHANCE_OF_ARTIST = 0.10;
        final double CHANCE_OF_HELPING_PROFESSION = 0.30;
        final double CHANCE_OF_BEING_UNEMPLOYED = 0.05;
        
        String name;
        String wantsThisJob;
        String wantsToMarry;
        String wantsChildren;
        String isRuleBreaker;
        String willKeepInTouchWithFriends;
        String willContributeToSociety;
        String societyLovesOrHates;
        String significantOther = null;
        String hasGoneToJail = null;
        String retire;
        String niceThings;
        String homeless;
        

        name = "What is your first name?";
        System.out.println(name);
        name = s.nextLine();
        System.out.println(name +","+ " Do you have a job?");
        wantsThisJob = s.nextLine();
        System.out.println("Are you homeless?");
        homeless = s.nextLine();
        System.out.println("Are you married?");
        wantsToMarry = s.nextLine();
        
        	if(wantsToMarry.equals("yes")) {
        		System.out.println("What is your significant others' name?");
        		significantOther = s.nextLine();

        	}else {
        		System.out.println("Do you plan on getting married in the future?");
        	}
        
        System.out.println("Do you have any children?");
        wantsChildren = s.nextLine();
        

        System.out.println("Are you planning on retiring?");
        retire = s.nextLine();
        System.out.println("Do you have any nice possessions?");
        niceThings = s.nextLine();
        System.out.println("Are you a rulebreaker?");
        isRuleBreaker = s.nextLine();
        
        if(isRuleBreaker.equals("yes")) {
        	System.out.println("Have you ever been to jail? (No judgement at all!) ");
        	hasGoneToJail = s.nextLine();
        	
        }if(isRuleBreaker.equals("no")) {
        	System.out.println("Thats good to hear :)"); }
        
        System.out.println("Will you keep in touch with your friends?");
        willKeepInTouchWithFriends = s.nextLine();
        System.out.println("Have you contributed to society?");
        willContributeToSociety = s.nextLine();
        System.out.println("Does society love or hate you? Please enter only 'loves' or 'hates.'");
        societyLovesOrHates = s.nextLine();
        
	  
	
        String actualJob = null;
        String actualWealth = null;
        boolean hasChildren;
        int numberOfChildren = 0;
        String child1n, child2n, child3n, child4n, child5n, child6n, child7n;
        String child1g, child2g, child3g, child4g, child5g, child6g, child7g;

		child1n = "Mohammad";
		child2n = "Ahmed";
		child3n = "Bilal";
		child4n = "Sara";
		child5n = "Aila";
		child6n = "Nusrat";
		child7n = "Aisha";

		child1g = "boy";
		child2g = "boy";
		child3g = "boy";
		child4g = "girl";
		child5g = "girl";
		child6g = "girl";
		child7g = "girl";


		double childProb = Math.random();
	
		if(childProb <= 0.30){
			hasChildren = false;
		} else {
			hasChildren = true;
			if(childProb > 0.30 && childProb <= 0.40){
				numberOfChildren = 1;
			} else if (childProb > 0.40 && childProb <= 0.50){
				numberOfChildren = 2;
			} else if (childProb > 0.50 && childProb <= 0.60){
				numberOfChildren = 3;
			} else if (childProb > 0.60 && childProb <= 0.70){
				numberOfChildren = 4;
			} else if (childProb > 0.70 && childProb <= 0.80){
				numberOfChildren = 5;
			} else if (childProb > 0.80 && childProb <= 0.90){
				numberOfChildren = 6;
			} else if (childProb > 0.9 && childProb <= 1){
				numberOfChildren = 7;
			}
		}
	


        final double occupationProbability = Math.random();
        
        if (occupationProbability <= 0.30){
            actualJob = BUSINESS_MAN;
        } else if (occupationProbability > 0.30 && occupationProbability <= 0.60){
            actualJob = HELPING_PROFESSION;
        } else if (occupationProbability > 0.60 && occupationProbability <= 0.65){
            actualJob = ENGINEER;
        } else if (occupationProbability > 0.65 && occupationProbability <= 0.75){
            actualJob = ARTIST;
        }
          else if (occupationProbability > 0.75 && occupationProbability <= 0.80){
        	actualJob = UNEMPLOYED;
        }
        
        switch(actualJob){
            case BUSINESS_MAN:
                if(Math.random() <= 0.70){
                    actualWealth = "rich";
                } else {
                    actualWealth = "in the middle class";
                }
                break;
            case ARTIST:
                if(Math.random() <= 0.10) {
                    actualWealth = "rich";
                } else{
                    actualWealth = "poor";
                }
                break;
            case ENGINEER:
                actualWealth = "rich";
                break;
            case HELPING_PROFESSION:
                actualWealth = "middle class";
                break;
            case UNEMPLOYED:
            	actualWealth = "poor";
            	break;
        }
        

        String lifeParagraph = "";
        lifeParagraph += name;
        lifeParagraph += " has a cool life. ";
        
          if(wantsToMarry.equals("yes")){
            lifeParagraph += (name + " is married to " + significantOther + ". ");
        } if(wantsToMarry.equals("no")){
        	lifeParagraph += (name + " doesn't want to get married. ");
        } 
          if(homeless.equals("yes")){
        	  lifeParagraph += (name + " is homeless. ");
          }if(homeless.equals("no")) {
        	  lifeParagraph += (name + " has a lovely home. ");
          }
        
        lifeParagraph += (name + " became " + actualJob +"." + " He/She was a " + actualWealth + " person. ");
        
        if(retire.equals("yes")) {
        	lifeParagraph += (name + " is planning on retiring soon. ");
        }
         if(retire.equals("no")) {
        	 lifeParagraph += (name + " is not planning on retire anytime soon. ");
         }
        
        if(willKeepInTouchWithFriends.equals("yes")) {
        	lifeParagraph += (name +" will keep in touch with her friends. ");
        }
        if(willContributeToSociety.equals("yes")) {
        	lifeParagraph += (name +" has contributed to society in many ways. ");
        }	
        	else {
        		System.out.println(name + " hasn't contributed to society.");
        	}
        
        
        if(societyLovesOrHates.equals("loves")) {
        	lifeParagraph += ("Society " + societyLovesOrHates + " " + name +". " );
        }
        else{
        	lifeParagraph += ("Society " + societyLovesOrHates + " " + name +". ");
        }
        
		if(hasGoneToJail.equals("yes")) {
			lifeParagraph +=  (name + " has been to jail. ");
		}

       
	if(hasChildren){
		
		lifeParagraph += "He/She had " + numberOfChildren + " children! ";
		if(wantsChildren.equals("yes")){
			lifeParagraph += "She/he is so happy and would love to have more kids! ";
		} else{
			lifeParagraph += "The children really stress him/her out! ";
		}
		
		if(numberOfChildren >= 1){
			lifeParagraph += "His/Her 1st child was named " + child1n + ". ";
			lifeParagraph += "It's a " + child1g + ". ";
		}

		if(numberOfChildren >= 2){
			lifeParagraph += "His/Her 2nd child was named " + child2n + ". ";
			lifeParagraph += "It's a " + child2g + ". ";
		}
		if(numberOfChildren >= 3){
			lifeParagraph += "His/Her 3rd child was named " + child3n + ". ";
			lifeParagraph += "It's a " + child3g + ". ";
		}
		if(numberOfChildren >= 4){
			lifeParagraph += "His/Her 4th child was named " + child4n + ". ";
			lifeParagraph += "It's a " + child4g + ". ";
		}
		if(numberOfChildren >= 5){
			lifeParagraph += "His/Her 5th child was named " + child5n + ". ";
			lifeParagraph += "It's a " + child5g + ". ";
		}
		if(numberOfChildren >= 6){
			lifeParagraph += "His/Her 6th child was named " + child6n + ". ";
			lifeParagraph += "It's a " + child6g + ". ";
		}
		if(numberOfChildren >= 7){
			lifeParagraph += "His/Her 7th child was named " + child7n + ". ";
			lifeParagraph += "It's a " + child7g + ". ";
		}

	} else {
		if(wantsChildren.equals("yes")){
			lifeParagraph += "He/She cried every night because they had no kids. :( ";
		} else{
			lifeParagraph += "He/She felt happier without any kids. ";
		}
		
	}
		if(niceThings.equals("yes")) {
			lifeParagraph += (name + " has many nice items at home. ");
			
		}
		if(niceThings.equals("no")) {
			lifeParagraph += (name + " does not own many nice items at home. ");
		}
        
        System.out.println(lifeParagraph);
    }
          
        
}



## Connect

If you want to reach out and chat, we definitely can! You can email me at nawal.nasir00@gmail.com!

