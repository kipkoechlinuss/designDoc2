
** Data Structures and Functions **

Add a fucntion that will parse the arguments and put it in an array to process.c. 


void parse_arguments(char *input)
 {
  char args [1024];
  char *tokens = strtok_r(input, " ");
  while(tokens != null){
  	args[i] = tokens;
	}
    }
   
  process_execute will create a user program with "filename" as the arguments. We will call the function we created 
  ```parse_arguments(filename) ``` to parse the user input and pushed them to the stack. We will also perform a check to see if the arguments are valid. 
** Algorithms **
In setup_stack() we call parse_arguments(char *input) where we will call strtok_r with a space
as the delimiter. We store each of these tokens in an array and increase our argc at the same time.
When we push these tokens onto the stack we start with the last one to the first one, pushing each pointer
onto the stack. This way, we will get each element of argv[] to be in the right order.
To avoid overflowing the stack page we limited the size of the total arguments to be less than
one page size (4 KB).


** Synchronization **




** ---- Rationale ---- **
We chose to use strtok_r instead of strtok because its thread safe
