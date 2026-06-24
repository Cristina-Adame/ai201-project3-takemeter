## Description of community, labels, and why these distinctions matter to people in that community. ##  
**Community** : 'r/CrossStitch' is a community where people who partake in the hobby of cross stitch will often post their works, questions, and ideas. 
Some people will go for inspiration or to look for help, but will often attach photos of their work. With proper labels, the user scrolling through the 
posts can decide if other users need help with their project, keep up with project progress of mutuals, and get inspiration from completed projects.  


**Labels** :    
  - _Finished Work:_ post where the user is sharing their completed crosstich pattern, normally including an image and excitement about the piece.
    
    - Examples:
      ```
      - 1. "Totoro. First project with backstitch, blended stitches, and fractional stitches.
            Substituted a color in the tree so it's a bit orangier than the pattern.
            https://www.etsy.com/listing/1074146954/totoro-pattern-pdf-cross-stitch-fantasy"
      ```
      ```
      - 2. "Kitty Litter pattern. Just finished my latest pattern from Dimensions, I started in January!
            I absolutely adore their animal patterns 🐱 I'm grateful 123stitch still carries them. Here
            are finished photos + the back and before finishing stitches."
      ```
      ```
      - 3. "New Chiikawa Cross Stitch. Just finished a new project. My cross stitch supplies are still
            being shipped to me from Japan to Brazil, but I got the cross stitch jitters and decided
            to get more supplies. First time working on 25 count evenweave! It's 2 over 1, half stitch,
            as recommended here in the past for full coverage projects. I used the Floss Cross website
            to help me make the pattern. Now moving on to a big project on 25 count!
      ```
    
  - _Work in Progress:_ post where the user will share an active, in-progress crosstitch project and normally including a photo and commentary on the progress.
    - Examples:
      ```
      - 1. "About 2/3rds through the stardew valley map! This one is a beast. Started it in February!
            Pattern: https://www.etsy.com/ca/listing/1843955177/new-stardew-valley-map-16-update-cross"
      ```
      ```
      - 2. "Haven't posted an update on this video large project in a while! Recently finished the
            first column and 10/50 pages!! About 9+ month of work. V happy its taking shape and im
            happy with my edits and color choices. I originally estimated 2 years but it will prob
            take quite a bit longer."
      ```
      ```
      - 3. "My progress on Venice by Luca-S. Hoping to finish this beauty by the end of summer!
            Slow but steady! This project is so detailed, but I'm absolutely loving how the colors
            are coming together.
            Decided to share my current progress here to stay motivated.
            My goal is to fully wrap it up by the end of August.
            Wish me luck!"
       ```    
  - _Chatting:_ post where user seeks advice about cross stitch techniques, information on materials or specific project ideas; can occasionally be written with no photo inclusion.
  - 
    - Examples:
      ```   
      - 1. "Michales has 40% off. For all you folks who need to kit out a project!"
      ```
      ```   
      - 2. "Thread vs Floss for Cross Stitch. I got into cross stitching/tatreez about a year ago now,
            but since it's a "slow" hobby I have only done about 2.5 projects. Two of which were part of a
            kit so I am still learning about the little things each day. Today I saw a thread about collecting
            and saw some people sharing pictures of their *thread* collections so now I am wondering-- is there a
            difference in using thread vs the split floss? Are they the same "size" if I wanted to use thread or
            are there differences my search hasn't pointed out?"
      
            Edit: IDK how different my question becomes when I mean sewing thread vs embroidery threads that
            come in the kits usually."
      ```
      ```   
      - 3. "A little question, I have experimented with the idea of finding a niche with cross stitching and I
            was wondering on doing microcross stitching, if that’s a thing? Has anyone done it, how small can you
            go (aida, thread, needle gauge), I kinda wanna see how far you can take it."
      ```      

**Distinctions** : 
  - These distinctions offer the users the ability to quickly nagivate to inspiration posts, follow along on other users' projects, learn about techniques used by others, and a way to label their posts so their questions may be replied to.


## Hardest Anticipated Edge Case ##
The hardest anticapted edge case will be the situation where a post includes a work in progress with a question included. It would be difficult to clearly exclusively label it as a work in progress when there is a chat-like question prompting information from other users. Specifying a decision rule that if an image is included in the post, it is considered a work in progress post since chat post are more likely to be exclusively text blocks.
  - Example:
    ```
    " [Image included]
      I'm working on a (mostly) self drafted pattern depicting the blazons of players and important NPC's from
      one of my TTRPG's. It's a gift for our gamemaster and I need to finish it in July. However, I'm not sure
      if I should add backstitching to it and if so , how/which colours? Tried metallic threads during a test,
      which made me rage quit.

      Any advice how to proceed? Leave like this or add backstitch?"
    ```
## Data Collection ##
Data will be manually collected from the subreddit 'r/CrossStitch' by searching through posts and copying the text into the CSV file. With the note if there is an inclusion of an image or not. For 200 examples, a close even split will be 67 of each type of label-specific post. 

## Evaluation Metrics## 
Since accuracy alone is not enough, the additional evaluation metric used will be F1 due to it taking into account precision and recall. Having a high metric in one will very obviously demonstrate the lack in the other and will provide insight into the evaluation of the model.

## Definition of Success ##
Since this is a form of filtering, success would be an F1 score of 0.7 and above. The data set is expected to be balanced leading to a high expected F1 score but with a small data set of 200, one mislabel can greatly affect the score of the model. Overall accuracy, success would be 75% to ensure the model is not making too many mistakes.

## AI Tool Plan ##
Plan to use Claude for label stress-testing to see if the handling of the hardest edge case was sufficient in situations where a post appears to be both work in progress and chat.
