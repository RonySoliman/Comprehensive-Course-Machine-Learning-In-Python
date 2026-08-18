# Titanic

Personally I find such datasets utterly compelling and heartbreaking, my logical side say don't get too attached. But information of this dataset isn't just numeric values, it's a complex story. I will leave you with a slice of a life that was once so vivid as this moment.

* I came across the feature `Ticket` and I wanted to understand if it's distinct value, could it be an identifier? Because in present each one has a unique combination of numbers combined to form a unique Ticket number. But it isn't the case here. I found the `Ticket` number `PC 17608`.
* My first instinct is that a wrong info, data quality thing.
* So I google one of the names listed `Ryerson, Mrs. Arthur Larned (Emily Maria Borie)`. Then it gets interesting! Apparently (Emily Maria Ryerson) is a survivor of Titanic sinking ship. She had a combination of magnificent and sad life. 
* The ticket number is a soociated with a cluster of sperated rooms more than a suite.
  
|index|PassengerId|Pclass|Name|Sex|Age|SibSp|Parch|Ticket|Fare|Embarked|
|---|---|---|---|---|---|---|---|---|---|---|
|24|916|1|Ryerson, Mrs\. Arthur Larned \(Emily Maria Borie\)|female|48\.0|1|3|PC 17608|262\.375|C|
|59|951|1|Chaudanson, Miss\. Victorine|female|36\.0|0|0|PC 17608|262\.375|C|
|64|956|1|Ryerson, Master\. John Borie|male|13\.0|2|2|PC 17608|262\.375|C|
|142|1034|1|Ryerson, Mr\. Arthur Larned|male|61\.0|1|3|PC 17608|262\.375|C|
|375|1267|1|Bowen, Miss\. Grace Scott|female|45\.0|0|0|PC 17608|262\.375|C|

* `Chaudanson, Miss. Victorine` was Emily's maid, and `Bowen, Miss. Grace Scott` was John (The Son) tutor and governess.
* That's why we see features like "SibSp" and "Parch" are labeled "0" for Victoria and Grace.

*[Here's the source in case you want to read it in more detail](https://www.encyclopedia-titanica.org/titanic-survivor/emily-ryerson.html)*
  
