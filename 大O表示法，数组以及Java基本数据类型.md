# Big O representation
### - the concept of time complexity
- time complexity means how much time will cost when running an program. The complexity is realted to the input size N. For example, if we have N data and we want to get the sum of those data, I need to scan all the data once, this will cost N, so the time complexity of this algorithm is O(N). Of course, time complexity could be a constant number, like add a data in Array or add constant data in Array.
### - an easy way to get the time complexity (few samples to remember)
- for loop | while loop
-
        for(int i=0; i<N; i++){
            //Do Something
        }//the time complexity is O(N)
- nested for|while loop
- 
        for(int i=0; i<N; i++){
            for(int j=0; j<N; j++){
                //Do Something
            }
        }//the time complexity is O(N^2)
- log factor
- 
        for(int i=0; i<N; i=i*a){ // a is a normal number. i.e. 2
            //Do something
        }//the time complexity is O(logN)
### - the example of Big O representation
- Binary search: O(logN)
- Qucik sort: O(NlogN)
- General Sort complexity: O(NlogN)
- .....
----------
# Array
### - concept
- Array is a data structure stored in a CONTINUE space in memory and it has a FIXED size. 
- Every element in Array has an INDEX, we can use this index to get this element. 
- Array could store any type of data.
- Array could store duplicated data
### - operations
        Array[] = Array[size] // initial the array
        Array[index] = element // add data into array
        element = Array[index] // get data from array
----------
# Java Basic Data Type
- there are few data type in Java and most of they have related object type
- 
        primitive type: float   Object: Float
        primitive type: double Object: Double
        primitive type: int    Object: Integer
        primitive type: boolean Object: Boolean
        primitive type: byte, short, long, char
--------
# Java Keywords
        abstract	continue	for	new	switch
        assert	default	goto	package	synchronized
        boolean	do	if	private	this
        break	double	implements	protected	throw
        byte	else	import	public	throws
        case	enum	instanceof	return	transient
        catch	extends	int	short	try
        char	final	interface	static	void
        class	finally	long	strictfp**	volatile
        const*	float	native	super	while
