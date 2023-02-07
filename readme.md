![HackerRank C Practice Rank](HackerRank%20C%20Practice%20Rank.png)
<h1><b>Solutions 👇</b></h1>
<h2><b>Hello World:  </b></h2>

```

#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() 
{
	
    char s[100];
    scanf("%[^\n]%*c", &s);
  	
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */    
    printf("Hello, World!\n");
    printf("Welcome to C programming.");
    return 0;
}

```

#

<h2><b>Playing With Characters:  </b></h2>

```
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>
#define MAX_LEN 128
int main() 
{
    char ch;
    char word[MAX_LEN];
    char sen[MAX_LEN];

    scanf("%c", &ch);
    scanf("%s\n", &word);
    scanf("%[^\n]%*c", &sen);

    printf("%c\n", ch);
    printf("%s\n", word);
    printf("%s\n", sen);

    return 0;

}


```

#

<h2><b> Sum and Difference of Two Numbers: </b></h2>

```
#include <stdio.h>
#include <math.h>

int main()
{
    int a,b;
    float c,d;
    scanf("%d%d",&a,&b);
    scanf("%f%f",&c,&d);
    printf("%d %d\n",a+b,a-b);
    printf("%.1f %.1f",c+d,c-d);
    return 0;

}

```

#

<h2><b> Functions in C: </b></h2>

```
#include <stdio.h>

#define max(a,b) (a>b?a:b)

int max_of_four(int a,int b,int c,int d){

    return max(a,max(b,max(c,d)));
}

int main() {

    int a, b, c, d;
    scanf("%d %d %d %d", &a, &b, &c, &d);
    int ans = max_of_four(a, b, c, d);
    printf("%d", ans);
    return 0;
}

```

#

<h2><b> Pointers In C: </b></h2>

```
#include <stdio.h>
#include <stdlib.h>

void update(int *a,int *b) {
    *a = *a+*b;
    *b = abs(*a-*b-*b);
}

int main() {
    int a, b;
    int *pa = &a, *pb = &b;
    
    scanf("%d %d", &a, &b);
    update(pa, pb);
    printf("%d\n%d", a, b);

    return 0;
}


```

#

<h2><b> Conditional Statements in C: </b></h2>

```
#include <stdio.h>
int main()
{
    int a;
    scanf("%d",&a);
    if (a<=9)
    {
        if (a==1)
        {
            printf("one");
            
        }
        if (a==2)
        {
            printf("two");
            
        }
        if (a==3)
        {
            printf("three");
           
        }
        if (a==4)
        {
            printf("four");
            
        }
        if (a==5)
        {
            printf("five");
            
        }
        if (a==6)
        {
            printf("six");
           
        }
        if (a==7)
        {
            printf("seven");
            
        }
        if (a==8)
        {
            printf("eight");
          
        }  
        if (a==9)
        {
            printf("nine");
          
        }
    }
    else
    {
        printf("Greater than 9");
    }
    return 0;
}

```

#

<h2><b> For Loop in C: </b></h2>

```
#include <stdio.h>
int main()
{
    int i,j,k;
    int a,b;
    char *ch[]={"null","one","two","three","four","five",
    "six","seven","eight","nine"};
    scanf("%d%d",&a,&b);

    for(i=a;i<=b;i++)
    {
        if(i>9 && i%2)
            printf("odd\n");
        else if(i>9 && i%2==0)
            printf("even\n");
        else
            printf("%s\n",ch[i]);

    }
    return 0;
}

```

#

<h2><b> Sum of Digits of a Five Digit Number: </b></h2>

```
#include <stdio.h>
int main()
{
    int i,j,k;
    int n;
    char s[6];

    scanf("%s",s);
    
    n=0;
    for(i=4;i>=0;i--)
   
        n+=(s[i]-'0');
    printf("%d",n);

    return 0;
}

```

#

<h2><b> Bitwise Operators: </b></h2>

```
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

void calculate_the_maximum(int n, int k) {
  int amax, omax, xmax;
  amax = omax = xmax = 0;
  for(int i = 1; i < n; i ++) {
      for(int j = i+1; j <= n; j ++) {
        amax = (i & j) > amax && (i & j) < k ? i & j : amax;
        omax = (i | j) > omax && (i | j) < k ? i | j : omax;
        xmax = (i ^ j) > xmax && (i ^ j) < k ? i ^ j : xmax; 
      }
  }
  printf("%d\n", amax);
  printf("%d\n", omax);
  printf("%d\n", xmax);
}

int main() {
    int n, k;
  
    scanf("%d %d", &n, &k);
    calculate_the_maximum(n, k);
 
    return 0;
}

```

#

<h2><b> Printing Pattern Using Loops: </b></h2>

```
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

void check(int i, int j, int first, int last, int n) {
  if(n >=1 ){
    if (i == first || i == last || j == first || j == last)
        printf("%d ", n);
    else
        check(i, j, first + 1, last - 1, n - 1);
  }
}

int main() 
{
    int n;
    scanf("%d", &n);
    int rows = 2 * n - 1;

    for (int i = 0; i < rows; i ++) {
        for (int j = 0; j < rows; j ++) {
            check(i, j, 0, rows - 1, n);
        }
        printf("\n");
    }
    return 0;
}


```

#

<h2><b> 1D Arrays in C: </b></h2>

```
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {
    int n, sum = 0;
    scanf("%d", &n);
    int * arr = (int *)malloc(n * sizeof(int));  
    for(int i = 0; i < n; i ++) {
        scanf("%d", arr + i);
        sum += arr [i];
    } 
    printf("%d", sum); 
    return 0;
}

```

#

<h2><b> Array Reversal: </b></h2>

```
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int num, *arr, i;
    scanf("%d", &num);
    arr = (int*) malloc(num * sizeof(int));
    for(i = 0; i < num; i++) {
        scanf("%d", arr + i);
    }

    for(int i = 0, j = num-1; i <= j; i++, j --) {
        int t = arr[i];
        arr[i] = arr [j];
        arr[j] = t;
    }

    for(i = 0; i < num; i++)
        printf("%d ", *(arr + i));
    return 0;
}

```

#

<h2><b> Printing Tokens: </b></h2>

```
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {

    char *s;
    s = malloc(1024 * sizeof(char));
    scanf("%[^\n]", s);
    s = realloc(s, strlen(s) + 1);
    for(int i = 0; i < strlen(s); i ++) {
        if(s[i] == ' ') s[i] = '\n';
    }
    printf("%s", s);
    free(s);
    return 0;
}

```

#

<h2><b> Digit Frequency: </b></h2>

```
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {

    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
    char s[1000];
    int arr[10] = {0};
    scanf("%s",s);
    
    for(int i = 0; i < strlen(s); i ++) {
        int j = s[i] - 48;
        if( j >= 0 && j <= 9 ) {
            arr[j]++;
        }
    }
    
    for(int i = 0; i < 10; i ++) {
        printf("%d ", arr[i]);
    }
    return 0;
}

```

#

<h2><b> Dynamic Array in C: </b></h2>

```

#include <stdio.h>
#include <stdlib.h>

/*
 * This stores the total number of books in each shelf.
 */
int* total_number_of_books;

/*
 * This stores the total number of pages in each book of each shelf.
 * The rows represent the shelves and the columns represent the books.
 */
int** total_number_of_pages;

int main()
{
    int total_number_of_shelves;
    scanf("%d", &total_number_of_shelves);
    
    int total_number_of_queries;
    scanf("%d", &total_number_of_queries);
    
    total_number_of_pages = (int **)malloc(total_number_of_shelves * sizeof(int*));
    
    total_number_of_books = (int *) malloc(total_number_of_shelves * sizeof(int));

    for(int i = 0; i < total_number_of_shelves; i ++) {
        total_number_of_books[i] = 0;
    }

    while (total_number_of_queries--) {
        int type_of_query;
        scanf("%d", &type_of_query);
        
        if (type_of_query == 1) {
            int x, y;
            scanf("%d %d", &x, &y);
            if(*(total_number_of_pages + x)) {
                *(total_number_of_pages + x) = (int *)realloc(*(total_number_of_pages + x), (total_number_of_books[x] + 1) * sizeof(int));
                total_number_of_pages[x][total_number_of_books[x]] = y;
            }
            else {
                *(total_number_of_pages + x) = (int *)malloc(sizeof(int));
                **(total_number_of_pages + x) = y;
            }
            total_number_of_books[x]++;
            
        } else if (type_of_query == 2) {
            int x, y;
            scanf("%d %d", &x, &y);
            printf("%d\n", *(*(total_number_of_pages + x) + y));
        } else {
            int x;
            scanf("%d", &x);
            printf("%d\n", *(total_number_of_books + x));
        }
    }

    if (total_number_of_books) {
        free(total_number_of_books);
    }
    
    for (int i = 0; i < total_number_of_shelves; i++) {
        if (*(total_number_of_pages + i)) {
            free(*(total_number_of_pages + i));
        }
    }
    
    if (total_number_of_pages) {
        free(total_number_of_pages);
    }
    
    return 0;
}


```

#

<h2><b> Calculate the Nth term: </b></h2>

```
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int find_nth_term(int n, int a, int b, int c) {
    if (n == 1) return a;
    if (n == 2) return b;
    if (n == 3) return c;
    else return(find_nth_term(n-1, a, b, c) + find_nth_term(n-2, a, b, c) + find_nth_term(n-3, a, b, c));
}

int main() {
    int n, a, b, c;
  
    scanf("%d %d %d %d", &n, &a, &b, &c);
    int ans = find_nth_term(n, a, b, c);
 
    printf("%d", ans); 
    return 0;
}

```

#

<h2><b> Students Marks Sum: </b></h2>

```
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int marks_summation(int* marks, int number_of_students, char gender) {
    int sum = 0;
    if (gender == 'b'){
        for(int i = 0; i < number_of_students; i += 2)  sum += marks[i];
    } else {
        for (int i = 1; i < number_of_students; i += 2) sum += marks[i];
    }
    return sum;
}

int main() {
    int number_of_students;
    char gender;
    int sum;
  
    scanf("%d", &number_of_students);
    int *marks = (int *) malloc(number_of_students * sizeof (int));
 
    for (int student = 0; student < number_of_students; student++) {
        scanf("%d", (marks + student));
    }
    
    scanf(" %c", &gender);
    sum = marks_summation(marks, number_of_students, gender);
    printf("%d", sum);
    free(marks);
 
    return 0;
}

```

#

<h2><b> Sorting Array of Strings: </b></h2>

```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int lexicographic_sort(const char* a, const char* b) {
    return (strcmp(a, b));
}

int lexicographic_sort_reverse(const char* a, const char* b) {
    return (strcmp(b, a));
}

int sort_by_number_of_distinct_characters(const char* a, const char* b) {
    int count[2] = {0};      //  array to maintain count of characters in a, b
    
    int presencea[26] = {0}; //  array to check presence of a character
    for (int j = 0; j < strlen(a); j++) {
        if (a[j] != ' ' && presencea[a[j] - 97] == 0) {
            presencea[a[j] - 97] = 1;
            count[0]++;
        }
    }

    int presenceb[26] = {0}; //  array to check presence of a character
    for (int j = 0; j < strlen(b); j++) {
        if (b[j] != ' ' && presenceb[b[j] - 97] == 0) {
            presenceb[b[j] - 97] = 1;
            count[1]++;
        }
    }

    if (count[0] > count[1] || (count[0] == count[1] && strcmp(a, b) > 0) ) return 1;
    else return 0;
}

int sort_by_length(const char* a, const char* b) {
    if(strlen(a) > strlen(b) ){
        return 1;
    } else if(strlen(a) == strlen(b)){
        if(strcmp(a, b) > 0) return 1;
        else return 0;
    } else return 0;
}

void string_sort(char** arr,const int len,int (*cmp_func)(const char* a, const char* b)){
    char * tmp;
    for(int i = 0; i < len - 1; i ++) {
        for (int j = i + 1; j < len ; j ++) 
            if(cmp_func(arr[i], arr[j] ) > 0){
                tmp = arr[i];
                arr[i] = arr[j];
                arr[j] = tmp; 
        }
    }    
}



int main() 
{
    int n;
    scanf("%d", &n);
  
    char** arr;
	arr = (char**)malloc(n * sizeof(char*));
  
    for(int i = 0; i < n; i++){
        *(arr + i) = malloc(1024 * sizeof(char));
        scanf("%s", *(arr + i));
        *(arr + i) = realloc(*(arr + i), strlen(*(arr + i)) + 1);
    }
  
    string_sort(arr, n, lexicographic_sort);
    for(int i = 0; i < n; i++)
        printf("%s\n", arr[i]);
    printf("\n");

    string_sort(arr, n, lexicographic_sort_reverse);
    for(int i = 0; i < n; i++)
        printf("%s\n", arr[i]); 
    printf("\n");

    string_sort(arr, n, sort_by_length);
    for(int i = 0; i < n; i++)
        printf("%s\n", arr[i]);    
    printf("\n");

    string_sort(arr, n, sort_by_number_of_distinct_characters);
    for(int i = 0; i < n; i++)
        printf("%s\n", arr[i]); 
    printf("\n");
}

```

#

<h2><b> Permutations of Strings </b></h2>

```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>


int next_permutation(int n, char **s)
{
    /**
    * Complete this method
    * Return 0 when there is no next permutation and 1 otherwise
    * Modify array s to its next permutation
    */
  int k, l;
  // 1. find the largest index k such that s[k] < s[k+1]
  for (k = n - 2; k >= 0; k --) {
    if(strcmp(s[k], s[k+1]) < 0) break;
  }
  if (k < 0) return 0;

  // 2. find the largest index l greater than k such that s[k] < s[l]
  for (l = n -1; l > k; l --) {
    if(strcmp(s[k], s[l]) < 0) break;
  }

  // 3. swap elements present at k, l
  char * tmp = s[k];
  s[k] = s[l];
  s[l] = tmp;

  // 4. reverse the sequence of elements from k+1 to n
  for(int i = k + 1, j = n -1; i < j; i ++, j --) {
    tmp = s[i];
    s[i] = s[j];
    s[j] = tmp;
  }
  return 1;
}

int main()
{
	char **s;
	int n;
	scanf("%d", &n);
	s = calloc(n, sizeof(char*));
	for (int i = 0; i < n; i++)
	{
		s[i] = calloc(11, sizeof(char));
		scanf("%s", s[i]);
	}
	do
	{
		for (int i = 0; i < n; i++)
			printf("%s%c", s[i], i == n - 1 ? '\n' : ' ');
	} while (next_permutation(n, s));
	for (int i = 0; i < n; i++)
		free(s[i]);
	free(s);
	return 0;
}

```

#

<h2><b> Variadic functions in C: </b></h2>

```
#include <stdarg.h>
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

#define MIN_ELEMENT 1
#define MAX_ELEMENT 1000000

int  sum (int count,...) {
    int sum = 0;

    // define a pointer to the variable list
    va_list ptr;
    // start the pointer to the list
    va_start(ptr, count);
    // access the argument pointed to in the list and increment position
    for (int i = 0; i < count; i ++) {
        sum += va_arg(ptr, int);
    }
    va_end(ptr);
    return sum;
}

int min(int count,...) {
    va_list ptr;
    va_start(ptr, count);
    
    int min = va_arg(ptr, int);
    int tmp;
    for(int i = 1; i < count; i ++) {
        if((tmp = va_arg(ptr, int)) < min) {
            min = tmp;
        }
    }
    va_end(ptr);
    return min;
}

int max(int count,...) {
    va_list ptr;
    va_start(ptr, count);
    
    int max = va_arg(ptr, int);
    int tmp;
    for(int i = 1; i < count; i ++) {
        if((tmp = va_arg(ptr, int)) > max) {
            max = tmp;
        }
    }
    va_end(ptr);
    return max;
}

int test_implementations_by_sending_three_elements() {
    srand(time(NULL));
    
    int elements[3];
    
    elements[0] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[1] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[2] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    
    fprintf(stderr, "Sending following three elements:\n");
    for (int i = 0; i < 3; i++) {
        fprintf(stderr, "%d\n", elements[i]);
    }
    
    int elements_sum = sum(3, elements[0], elements[1], elements[2]);
    int minimum_element = min(3, elements[0], elements[1], elements[2]);
    int maximum_element = max(3, elements[0], elements[1], elements[2]);

    fprintf(stderr, "Your output is:\n");
    fprintf(stderr, "Elements sum is %d\n", elements_sum);
    fprintf(stderr, "Minimum element is %d\n", minimum_element);
    fprintf(stderr, "Maximum element is %d\n\n", maximum_element);
    
    int expected_elements_sum = 0;
    for (int i = 0; i < 3; i++) {
        if (elements[i] < minimum_element) {
            return 0;
        }
        
        if (elements[i] > maximum_element) {
            return 0;
        }
        
        expected_elements_sum += elements[i];
    }
    
    return elements_sum == expected_elements_sum;
}

int test_implementations_by_sending_five_elements() {
    srand(time(NULL));
    
    int elements[5];
    
    elements[0] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[1] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[2] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[3] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[4] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    
    fprintf(stderr, "Sending following five elements:\n");
    for (int i = 0; i < 5; i++) {
        fprintf(stderr, "%d\n", elements[i]);
    }
    
    int elements_sum = sum(5, elements[0], elements[1], elements[2], elements[3], elements[4]);
    int minimum_element = min(5, elements[0], elements[1], elements[2], elements[3], elements[4]);
    int maximum_element = max(5, elements[0], elements[1], elements[2], elements[3], elements[4]);
    
    fprintf(stderr, "Your output is:\n");
    fprintf(stderr, "Elements sum is %d\n", elements_sum);
    fprintf(stderr, "Minimum element is %d\n", minimum_element);
    fprintf(stderr, "Maximum element is %d\n\n", maximum_element);
    
    int expected_elements_sum = 0;
    for (int i = 0; i < 5; i++) {
        if (elements[i] < minimum_element) {
            return 0;
        }
        
        if (elements[i] > maximum_element) {
            return 0;
        }
        
        expected_elements_sum += elements[i];
    }
    
    return elements_sum == expected_elements_sum;
}

int test_implementations_by_sending_ten_elements() {
    srand(time(NULL));
    
    int elements[10];
    
    elements[0] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[1] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[2] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[3] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[4] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[5] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[6] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[7] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[8] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    elements[9] = rand() % (MAX_ELEMENT - MIN_ELEMENT + 1) + MIN_ELEMENT;
    
    fprintf(stderr, "Sending following ten elements:\n");
    for (int i = 0; i < 10; i++) {
        fprintf(stderr, "%d\n", elements[i]);
    }
    
    int elements_sum = sum(10, elements[0], elements[1], elements[2], elements[3], elements[4],
                           elements[5], elements[6], elements[7], elements[8], elements[9]);
    int minimum_element = min(10, elements[0], elements[1], elements[2], elements[3], elements[4],
                           elements[5], elements[6], elements[7], elements[8], elements[9]);
    int maximum_element = max(10, elements[0], elements[1], elements[2], elements[3], elements[4],
                           elements[5], elements[6], elements[7], elements[8], elements[9]);
    
    fprintf(stderr, "Your output is:\n");
    fprintf(stderr, "Elements sum is %d\n", elements_sum);
    fprintf(stderr, "Minimum element is %d\n", minimum_element);
    fprintf(stderr, "Maximum element is %d\n\n", maximum_element);
    
    int expected_elements_sum = 0;
    for (int i = 0; i < 10; i++) {
        if (elements[i] < minimum_element) {
            return 0;
        }
        
        if (elements[i] > maximum_element) {
            return 0;
        }
        
        expected_elements_sum += elements[i];
    }
    
    return elements_sum == expected_elements_sum;
}

int main ()
{
    int number_of_test_cases;
    scanf("%d", &number_of_test_cases);
    
    while (number_of_test_cases--) {
        if (test_implementations_by_sending_three_elements()) {
            printf("Correct Answer\n");
        } else {
            printf("Wrong Answer\n");
        }
        
        if (test_implementations_by_sending_five_elements()) {
            printf("Correct Answer\n");
        } else {
            printf("Wrong Answer\n");
        }
        
        if (test_implementations_by_sending_ten_elements()) {
            printf("Correct Answer\n");
        } else {
            printf("Wrong Answer\n");
        }
    }
    
    return 0;
}

```

#

<h2><b> Querying the Document: </b></h2>

```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include<assert.h>
#define MAX_CHARACTERS 1005
#define MAX_PARAGRAPHS 5

char* kth_word_in_mth_sentence_of_nth_paragraph(char**** document, int k, int m, int n) {
    return document[n - 1][m - 1][k - 1];
}

char** kth_sentence_in_mth_paragraph(char**** document, int k, int m) {
    return document[m - 1][k - 1];
}

char*** kth_paragraph(char**** document, int k) {
    return document[k - 1];
}

char**** get_document(char* text) {
    // doc points to an array of paragraphs
    char ****doc = malloc(MAX_PARAGRAPHS * sizeof(char ***)); 

    // for each paragraph, assign an array of 1 sentence, we can reallocate later
    for(int i = 0; i < MAX_PARAGRAPHS; i ++) {
        doc[i] = malloc(1 * sizeof(char **));
    }

    // for each sentence assign an array of 1 word
    for(int i = 0; i < MAX_PARAGRAPHS; i ++) {
        for(int j = 0; j < 1; j ++) {
            doc[i][j] = malloc(1 * sizeof(char*));
        }
    }

    // for each word assign an array of 1 character
    for(int i = 0; i < MAX_PARAGRAPHS; i ++) {
        for(int j = 0; j < 1; j ++) {
            for(int k = 0; k < 1; k ++) {
                doc[i][j][k] = malloc(1 * sizeof(char));
            }
        }
    }
     
    for(int n = 0, i = 0, j = 0, k = 0, l = 0; n < strlen(text); n ++) {
        if(text[n] != ' ' && text[n] != '\n' && text[n] != '.') {
            doc[i][j][k][l] = text[n];
            l++;
            doc[i][j][k] = realloc(doc[i][j][k], (l + 1) * sizeof(char));
        } else if(text[n] == ' ') {
            doc[i][j][k][l] = '\0';
            l = 0;
            k++;
            doc[i][j] = realloc(doc[i][j], (k + 1) * sizeof(char*));
            doc[i][j][k] = malloc(sizeof(char));
            continue;
        } else if(text[n] == '.') {
            doc[i][j][k][l] = '\0';
            k = l = 0;
            j++;
            doc[i] = realloc(doc[i], (j+1) * sizeof(char**));
            doc[i][j] = malloc(sizeof(char*));
            doc[i][j][k] = malloc(sizeof(char));
            continue;
        } else if(text[n] == '\n') {
            j = k = l = 0;
            i++;
            continue;
        }
    }
    return doc;
}



char* get_input_text() {	
    int paragraph_count;
    scanf("%d", &paragraph_count);

    char p[MAX_PARAGRAPHS][MAX_CHARACTERS], doc[MAX_CHARACTERS];
    memset(doc, 0, sizeof(doc));
    getchar();
    for (int i = 0; i < paragraph_count; i++) {
        scanf("%[^\n]%*c", p[i]);
        strcat(doc, p[i]);
        if (i != paragraph_count - 1)
            strcat(doc, "\n");
    }

    char* returnDoc = (char*)malloc((strlen (doc)+1) * (sizeof(char)));
    strcpy(returnDoc, doc);
    return returnDoc;
}

void print_word(char* word) {
    printf("%s", word);
}

void print_sentence(char** sentence) {
    int word_count;
    scanf("%d", &word_count);
    for(int i = 0; i < word_count; i++){
        printf("%s", sentence[i]);
        if( i != word_count - 1)
            printf(" ");
    }
} 

void print_paragraph(char*** paragraph) {
    int sentence_count;
    scanf("%d", &sentence_count);
    for (int i = 0; i < sentence_count; i++) {
        print_sentence(*(paragraph + i));
        printf(".");
    }
}

int main() 
{
    char* text = get_input_text();
    char**** document = get_document(text);

    int q;
    scanf("%d", &q);

    while (q--) {
        int type;
        scanf("%d", &type);

        if (type == 3){
            int k, m, n;
            scanf("%d %d %d", &k, &m, &n);
            char* word = kth_word_in_mth_sentence_of_nth_paragraph(document, k, m, n);
            print_word(word);
        }

        else if (type == 2){
            int k, m;
            scanf("%d %d", &k, &m);
            char** sentence = kth_sentence_in_mth_paragraph(document, k, m);
            print_sentence(sentence);
        }

        else{
            int k;
            scanf("%d", &k);
            char*** paragraph = kth_paragraph(document, k);
            print_paragraph(paragraph);
        }
        printf("\n");
    }     
}


```

#

<h2><b> Boxes through a Tunnel: </b></h2>

```
#include <stdio.h>
#include <stdlib.h>
#define MAX_HEIGHT 41


struct box
{
    int length;
    int height;
    int width;
};

typedef struct box box;

int get_volume(box b) {
    return (b.length * b.height * b.width);
}

int is_lower_than_max_height(box b) {
    if(b.height < MAX_HEIGHT) return 1;
    else return 0;
}


int main()
{
	int n;
	scanf("%d", &n);
	box *boxes = malloc(n * sizeof(box));
	for (int i = 0; i < n; i++) {
		scanf("%d%d%d", &boxes[i].length, &boxes[i].width, &boxes[i].height);
	}
	for (int i = 0; i < n; i++) {
		if (is_lower_than_max_height(boxes[i])) {
			printf("%d\n", get_volume(boxes[i]));
		}
	}
	return 0;
}

```

#

<h2><b> Small Triangles, Large Triangles: </b></h2>

```
#include <stdio.h>
#include <stdlib.h>
#include <math.h>

struct triangle
{
	int a;
	int b;
	int c;
};

typedef struct triangle triangle;

int area(triangle t) {
    return((t.a+t.b+t.c)*(t.a+t.b-t.c)*(t.a+t.c-t.b)*(t.b+t.c-t.a)); 
}

void sort_by_area(triangle* tr, int n) {
    /**
    * Sort an array a of the length n
    */

    for(int i = 0; i < n - 1; i ++) 
        for(int j = i + 1; j < n; j ++)
            if(area(tr[i]) > area(tr[j])) {
                triangle t = tr[i];
                tr[i] = tr[j];
                tr[j] = t;
            }
}

int main()
{
	int n;
	scanf("%d", &n);
	triangle *tr = malloc(n * sizeof(triangle));
	for (int i = 0; i < n; i++) {
		scanf("%d%d%d", &tr[i].a, &tr[i].b, &tr[i].c);
	}
	sort_by_area(tr, n);
	for (int i = 0; i < n; i++) {
		printf("%d %d %d\n", tr[i].a, tr[i].b, tr[i].c);
	}
	return 0;
}

```

#

<h2><b> Post Transition: </b></h2>

```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#define MAX_STRING_LENGTH 6

struct package
{
    char* id;
    int weight;
};

typedef struct package package;

struct post_office
{
    int min_weight;
    int max_weight;
    package* packages;
    int packages_count;
};

typedef struct post_office post_office;

struct town
{
    char* name;
    post_office* offices;
    int offices_count;
};

typedef struct town town;

void print_all_packages(town t) {
    printf("%s:\n", t.name);
    for(int i = 0; i < t.offices_count; i ++) {
        printf("\t%d:\n", i);
        for(int j = 0; j < t.offices[i].packages_count; j ++) {
            printf("\t\t%s\n", t.offices[i].packages[j].id);
        }
    }
}

void send_all_acceptable_packages(town* source, int source_office_index, town* target, int target_office_index) {
   
    int min = target -> offices[target_office_index].min_weight;
    int max = target -> offices[target_office_index].max_weight;
    
    for(int i = 0; i < source -> offices[source_office_index].packages_count ; i ++) {
        int weight = source -> offices[source_office_index].packages[i].weight;
        if(weight >= min && weight <= max) {
            target -> offices[target_office_index].packages = realloc(target -> offices[target_office_index].packages, (target -> offices[target_office_index].packages_count + 1) * sizeof(package));
            target -> offices[target_office_index].packages[target -> offices[target_office_index].packages_count] = source -> offices[source_office_index].packages[i];
            (target -> offices[target_office_index].packages_count)++;
            
            for(int j = i; j < source -> offices[source_office_index].packages_count - 1; j ++) {
                source -> offices[source_office_index].packages[j] = source -> offices[source_office_index].packages[j+1];
            }
            source -> offices[source_office_index].packages = realloc(source -> offices[source_office_index].packages, (source -> offices[source_office_index].packages_count - 1)* sizeof(package));
            source -> offices[source_office_index].packages_count --;
            i--;
        }
    }
}

town town_with_most_packages(town* towns, int towns_count) {
    int index = 0, max = 0;
    for(int i = 0; i < towns_count; i ++) {
        int sum = 0;
        for(int j = 0; j < towns[i].offices_count; j ++) {
            sum += towns[i].offices[j].packages_count;
        }
        if(sum > max) {
            max = sum;
            index = i;
        }
    }
    return  towns[index];
}

town* find_town(town* towns, int towns_count, char* name) {
    int i;
    for(i = 0; i < towns_count; i ++) {
        if(! (strcmp(towns[i].name, name)) ) break;
    }
    return towns + i;
}

int main()
{
    int towns_count;
    scanf("%d", &towns_count);
    town* towns = malloc(sizeof(town)*towns_count);
    for (int i = 0; i < towns_count; i++) {
        towns[i].name = malloc(sizeof(char) * MAX_STRING_LENGTH);
        scanf("%s", towns[i].name);
        scanf("%d", &towns[i].offices_count);
        towns[i].offices = malloc(sizeof(post_office)*towns[i].offices_count);
        for (int j = 0; j < towns[i].offices_count; j++) {
            scanf("%d%d%d", &towns[i].offices[j].packages_count, &towns[i].offices[j].min_weight, &towns[i].offices[j].max_weight);
            towns[i].offices[j].packages = malloc(sizeof(package)*towns[i].offices[j].packages_count);
            for (int k = 0; k < towns[i].offices[j].packages_count; k++) {
                towns[i].offices[j].packages[k].id = malloc(sizeof(char) * MAX_STRING_LENGTH);
                scanf("%s", towns[i].offices[j].packages[k].id);
                scanf("%d", &towns[i].offices[j].packages[k].weight);
            }
        }
    }
    int queries;
    scanf("%d", &queries);
    char town_name[MAX_STRING_LENGTH];
    while (queries--) {
        int type;
        scanf("%d", &type);
        switch (type) {
            case 1:
                scanf("%s", town_name);
                town* t = find_town(towns, towns_count, town_name);
                print_all_packages(*t);
                break;
            case 2:
                scanf("%s", town_name);
                town* source = find_town(towns, towns_count, town_name);
                int source_index;
                scanf("%d", &source_index);
                scanf("%s", town_name);
                town* target = find_town(towns, towns_count, town_name);
                int target_index;
                scanf("%d", &target_index);
                send_all_acceptable_packages(source, source_index, target, target_index);
                break;
            case 3:
                printf("Town with the most number of packages is %s\n", town_with_most_packages(towns, towns_count).name);
                break;
        }
    }
    for(int i = 0; i < towns_count; i ++) {
        for (int j = 0; j < towns[i].offices_count; j ++) {
                free(towns[i].offices[j].packages);
        }
        free(towns[i].offices);
    }
    free(towns);
    return 0;
}

```

#

<h2><b> Structuring the Document: </b></h2>

```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <assert.h>
#define MAX_CHARACTERS 1005
#define MAX_PARAGRAPHS 5

struct word {
    char* data;
};

struct sentence {
    struct word* data;
    int word_count;//denotes number of words in a sentence
};

struct paragraph {
    struct sentence* data  ;
    int sentence_count;//denotes number of sentences in a paragraph
};

struct document {
    struct paragraph* data;
    int paragraph_count;//denotes number of paragraphs in a document
};


struct document get_document(char* text) {
     struct document doc;

    int pcount = 0;
    for(int i = 0; i < strlen(text) ; i ++) {
        if(text[i] == '\n') pcount ++;
    }
    pcount ++;

    doc.paragraph_count = pcount;
    doc.data = malloc(pcount * sizeof(struct paragraph));

    for(int n = 0, m = 0, l = 0, i = 0; i < pcount; i ++) {
        int scount = 0;
        while(text[n] != '\n' && n < strlen(text)) {
            if(text[n] == '.') scount ++;
            n ++;
        }
        n ++;

        doc.data[i].sentence_count = scount;
        doc.data[i].data = malloc(scount * sizeof(struct sentence));

        for(int j = 0; j < scount; j ++) {
            int wcount = 0;
            while(text[m] != '.' && m < n) {
                if(text[m] == ' ') wcount ++;
                m ++;
            }
            m ++;
            if(text[m] == '\n') m ++;
            wcount ++;

            doc.data[i].data[j].word_count = wcount;
            doc.data[i].data[j].data = malloc(wcount * sizeof(struct word));

            for(int k = 0; k < wcount; k ++) {
                int ccount = 0;
                while(text[l] != ' ' && text[l] != '.' && l < m) {
                    ccount ++;
                    l ++;
                }
                l ++;
                if(text[l] == '\n') l ++;

                ccount ++;
                doc.data[i].data[j].data[k].data = malloc(ccount * sizeof(char));
            }
        }
    }

    int r = 0;
    for(int i = 0; i < doc.paragraph_count; i ++) {
        for(int j = 0; j < doc.data[i].sentence_count; j ++) {
            for(int k = 0; k < doc.data[i].data[j].word_count; k ++) {
                int l = 0;
                while(text[r] != ' ' && text[r] != '.' && text[r] != '\n') {
                    doc.data[i].data[j].data[k].data[l] = text[r];
                    r++;
                    l++;
                }
                doc.data[i].data[j].data[k].data[l] = '\0';
                if(text[r] == '.') {
                    r++;
                    break;
                }
                r ++;
            }
            if(text[r] == '\n') {
                r ++;
                break;
            }
        }
    }

    return doc;
}

struct word kth_word_in_mth_sentence_of_nth_paragraph(struct document Doc, int k, int m, int n) {
    return Doc.data[n - 1].data[m - 1].data[k - 1];
}

struct sentence kth_sentence_in_mth_paragraph(struct document Doc, int k, int m) { 
    return Doc.data[m - 1].data[k - 1];
}

struct paragraph kth_paragraph(struct document Doc, int k) {
    return Doc.data[k - 1];
}


void print_word(struct word w) {
    printf("%s", w.data);
}

void print_sentence(struct sentence sen) {
    for(int i = 0; i < sen.word_count; i++) {
        print_word(sen.data[i]);
        if (i != sen.word_count - 1) {
            printf(" ");
        }
    }
}

void print_paragraph(struct paragraph para) {
    for(int i = 0; i < para.sentence_count; i++){
        print_sentence(para.data[i]);
        printf(".");
    }
}

void print_document(struct document doc) {
    for(int i = 0; i < doc.paragraph_count; i++) {
        print_paragraph(doc.data[i]);
        if (i != doc.paragraph_count - 1)
            printf("\n");
    }
}

char* get_input_text() {	
    int paragraph_count;
    scanf("%d", &paragraph_count);

    char p[MAX_PARAGRAPHS][MAX_CHARACTERS], doc[MAX_CHARACTERS];
    memset(doc, 0, sizeof(doc));
    getchar();
    for (int i = 0; i < paragraph_count; i++) {
        scanf("%[^\n]%*c", p[i]);
        strcat(doc, p[i]);
        if (i != paragraph_count - 1)
            strcat(doc, "\n");
    }

    char* returnDoc = (char*)malloc((strlen (doc)+1) * (sizeof(char)));
    strcpy(returnDoc, doc);
    return returnDoc;
}

int main() 
{
    char* text = get_input_text();
    struct document Doc = get_document(text);

    int q;
    scanf("%d", &q);

    while (q--) {
        int type;
        scanf("%d", &type);

        if (type == 3){
            int k, m, n;
            scanf("%d %d %d", &k, &m, &n);
            struct word w = kth_word_in_mth_sentence_of_nth_paragraph(Doc, k, m, n);
            print_word(w);
        }

        else if (type == 2) {
            int k, m;
            scanf("%d %d", &k, &m);
            struct sentence sen= kth_sentence_in_mth_paragraph(Doc, k, m);
            print_sentence(sen);
        }

        else{
            int k;
            scanf("%d", &k);
            struct paragraph para = kth_paragraph(Doc, k);
            print_paragraph(para);
        }
        printf("\n");
    }     
}

```