# assignment2-mohammed
# Mohammed Shahid
###### Hyderabad
at over 12.2 million, it has the largest population of any city in the state Hyderabad is an A-1 city under the terms of development priorities. It is also known as **city of pearls or city of Nizams**. The people of Hyderabad are called **Hyderabadis**.


***
# Travel Instructions
1. The fastest and safest travel would be through flight,  
    1. first we need to book flight from LA to hyderabad
    2. after reaching to hyderabad airport, book a uber cab in airport.
    3. The cab driver we will be there in minutes before checking into the cab we need to give the otp.
2. The cab driver will drop you at the charminar.

***
# Unordered List

* Go to store
    * Buy food
        * pizza
        * candies
        * chicken 
        * cookies
        * cool drinks
    * Buy clothing
        * shoes
        * jackets
        * tents

**[ABOUT ME](AboutMe.md)**

***

# Tables

## showing table format
<br>
This is a table showing the data related to my favourite items 
where I would recommend to someone.

|FOODS|LOCATION|AMOUNT|
|---|---|---|
|Pizza|Dominos Pizza|$20|
|Burger|Bburger King|$10|
|Pasta|Wall Mart|$5|
|Biryani|Bawarchi|$15|

*** 

## Pithy Quotes

> That which does not kill us makes us stronger.
- *Friedrich Nietzsche*

> We must not allow other people’s limited perceptions to define us.
- *Virginia Satir*

***
## code fencing

    int m, n;  
    vector<long long> dp_before(n), dp_cur(n);  

    long long C(int i, int j);  

    // compute dp_cur[l], ... dp_cur[r] (inclusive)
    void compute(int l, int r, int optl, int optr) {
        if (l > r)
            return;

        int mid = (l + r) >> 1;
        pair<long long, int> best = {LLONG_MAX, -1};

        for (int k = optl; k <= min(mid, optr); k++) {
            best = min(best, {(k ? dp_before[k - 1] : 0) + C(k, mid), k});
        }

        dp_cur[mid] = best.first;
        int opt = best.second;

        compute(l, mid - 1, optl, opt);
        compute(mid + 1, r, opt, optr);
    }


> In both contexts it refers to simplifying a complicated problem by breaking it down into simpler sub-problems in a recursive manner. While some decision problems cannot be taken apart this way, decisions that span several points in time do often break apart recursively. Likewise, in computer science, if a problem can be solved optimally by breaking it into sub-problems and then recursively finding the optimal solutions to the sub-problems, then it is said to have optimal substructure.

[dynamic programming](https://en.wikipedia.org/wiki/Dynamic_programming)

var m := map(0 → 0, 1 → 1)  
  function fib(n)  
      if key n is not in map m  
          m[n] := fib(n − 1) + fib(n − 2)  
      return m[n]  
[Code Source](https://en.wikipedia.org/wiki/Dynamic_programming)

    


