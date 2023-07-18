& and * new syntax

to find the address and access

treat addresses as numbers and poke around with computer memory

```c
include <stdio.h>

int main(void)
{
cjar *s = "HI!";
printf("%s\n", *s);
printf("%s\n", *(s+1*));
}
```

malloc to request to reserve memory

free to free the remaining extra memory previously requested

malloc and free from <stdlib.h>

```c
int main(void)
{
char *s = get_string("s: ");
char *t = malloc(strlen(s) + 1);

for (int i = 0; i < strlen(s) + 1; i++)
	{
	t[i] = s[i];
	}

if (strlen(t) > 0)
	{
	t[0] = toupper(s[0]);
	}
}
```

C has two powerful operators that relate to memory
& provides the address of something stored in memory
/*/ instructs the compiler to go to a location in memory


**Data structures**

hash tables - combine the random access ability of an array with the dynamism of a lined list 

for a hash table we need:
- a hash function, which returns nonnegative integer value
- an array capable of storing data of the type we wish to place into the data structure

we take data. we put it through the function. it spits a number (preferred location in the set)

```c
unsigned int hash(char* str)
{
	int sum = 0;
	for (int j = 0; str[j] != "\0"; j++)
	{
		sum += str[j];
	}
	return sum % HASH_MAX;
}
```

```c
node *hashtable[10];
hash("Joey");
//returns 6;
```