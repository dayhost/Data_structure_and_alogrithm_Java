# Sorting Allgorithm
### Bubble Sort
- Bubble sort, from the name we could know that it is like bubble poping from a cup of coke, the biggest come out first and the second biggest, etc until all the bubble(element) pops out.
- [Bubble sort](https://www.tutorialspoint.com/data_structures_algorithms/bubble_sort_algorithm.htm)
### Merge Sort
- Merge sort is merge two SORTED list into one SORTED list. The precondition is that we already have two sorted list.
- [merge sort](https://www.tutorialspoint.com/data_structures_algorithms/merge_sort_algorithm.htm)
### Insert Sort
- Insert sort scan the array and divide it into 2 parts: sorted part and unsorted part. If it find a bigger element in the unsorted part, insert into the sorted part in the front.
- [insert sort](https://www.tutorialspoint.com/data_structures_algorithms/insertion_sort_algorithm.htm)
### Select Sort
- select sort scan the whole list and divide the list into two parts. If it finds a smaller element than the current element, it will swap them.
### Select Sort[https://www.tutorialspoint.com/data_structures_algorithms/selection_sort_algorithm.htm]
### Quick sort
- this algorithm is a little complex, cause it used a strage called divide and conquer. It also divide the list into two parts but this algorithm do it ieratively.
- Quick sort[https://www.tutorialspoint.com/data_structures_algorithms/quick_sort_algorithm.htm]
--------
# Java Control Flow
### if-else
        if(condition1){
            //do something
        }else if(condition2){
            //do something
        }else{
            //do something
        }
### switch
        switch(conditon){
            case 1: 
                break;
            case 2:
                break;
        }
### while
        while(condition){
            //do something
        }
### for
        for(int i=0; i<N; i++){
            //do something
        }
### do-while
        do{
            //do something
        }while(condition);
- the different between while and do-while is that do while do the statement frist and then evaluate the condition and while do the evaluation frsit.
### break statement & continue statement
        break; //jump out from the whole loop
        continue; // jump out from this loop and jump into next loop
### try-catch
        try{
            // something that could go wrong
        }catch(Exception e){
            // do some error process
        }
