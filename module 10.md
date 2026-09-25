EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:
```
    printf("Enter the number of nodes: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        newNode = (struct Node *)malloc(sizeof(struct Node));

        printf("Enter element %d: ", i + 1);
        scanf("%d", &newNode->data);

        newNode->next = NULL;

        if (head == NULL)
        {
            head = newNode;
        }
        else
        {
            temp = head;

            while (temp->next != NULL)
            {
                temp = temp->next;
            }

            temp->next = newNode;
        }
    }

    printf("Enter the element to search: ");
    scanf("%d", &search);

    temp = head;

    while (temp != NULL)
    {
        if (temp->data == search)
        {
            printf("Element %d found at position %d.\n",
                   search, position);
            found = 1;
            break;
        }

        temp = temp->next;
        position++;
    }

    if (found == 0)
    {
        printf("Element %d not found in the linked list.\n", search);
    }

    return 0;
}
```

Output:

<img width="853" height="426" alt="image" src="https://github.com/user-attachments/assets/062b0393-c067-4aa4-94af-ccef6ff1e78d" />




Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:
```
#include <stdio.h> #include <stdlib.h>

struct Node { int data; struct Node *next; };

void insert(struct Node **head, int value) { struct Node *newNode; struct Node *temp;

    newNode = (struct Node *)malloc(sizeof(struct Node));

    newNode->data = value;
    newNode->next = NULL;

    if (*head == NULL)
    {
        *head = newNode;
    }
    else
    {
        temp = *head;

        while (temp->next != NULL)
        {
            temp = temp->next;
        }

        temp->next = newNode;
    }
}
void display(struct Node *head) { struct Node *temp = head;

    while (temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }
}
int main() { struct Node *head = NULL; int n, i, value;

    printf("Enter the number of nodes: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        printf("Enter element %d: ", i + 1);
        scanf("%d", &value);

        insert(&head, value);
    }

    printf("\nLinked list after insertion:\n");
    display(head);

    return 0;
}
```

Output:

<img width="847" height="393" alt="image" src="https://github.com/user-attachments/assets/61e0f924-c46e-4010-b503-4f03880e51f9" />


 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

```
    printf("Enter the number of nodes: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        newNode = (struct Node *)malloc(sizeof(struct Node));

        printf("Enter element %d: ", i + 1);
        scanf("%d", &newNode->data);

        newNode->prev = NULL;
        newNode->next = NULL;

        if (head == NULL)
        {
            head = newNode;
        }
        else
        {
            temp = head;

            while (temp->next != NULL)
            {
                temp = temp->next;
            }

            temp->next = newNode;
            newNode->prev = temp;
        }
    }

    printf("\nDoubly linked list elements:\n");

    temp = head;

    while (temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }

    return 0;
}
```

Output:

<img width="840" height="382" alt="image" src="https://github.com/user-attachments/assets/b78a4dc9-50f7-4d00-a3eb-23140d543a4a" />



Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:

```
#include <stdio.h> #include <stdlib.h>

struct Node { int data; struct Node *prev; struct Node *next; };

void insert(struct Node **head, int value) { struct Node *newNode; struct Node *temp;

    newNode = (struct Node *)malloc(sizeof(struct Node));

    newNode->data = value;
    newNode->prev = NULL;
    newNode->next = NULL;

    if (*head == NULL)
    {
        *head = newNode;
    }
    else
    {
        temp = *head;

        while (temp->next != NULL)
        {
            temp = temp->next;
        }

        temp->next = newNode;
        newNode->prev = temp;
    }
}
void display(struct Node *head) { struct Node *temp = head;

    while (temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }
}
int main() { struct Node *head = NULL; int n, i, value;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        printf("Enter element %d: ", i + 1);
        scanf("%d", &value);

        insert(&head, value);
    }

    printf("\nDoubly linked list after insertion:\n");
    display(head);

    return 0;
}
```

Output:

<img width="855" height="442" alt="image" src="https://github.com/user-attachments/assets/dc547508-39a2-4a96-9d1f-cbd9e7695652" />



Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:
```
#include <stdio.h> #include <stdlib.h>

struct Node { int data; struct Node *next; };

void deleteElement(struct Node **head, int value) { struct Node *temp; struct Node *prev;

    if (*head == NULL)
    {
        printf("Linked list is empty.\n");
        return;
    }

    temp = *head;
    prev = NULL;

    while (temp != NULL && temp->data != value)
    {
        prev = temp;
        temp = temp->next;
    }

    if (temp == NULL)
    {
        printf("Element %d not found.\n", value);
        return;
    }

    if (prev == NULL)
    {
        *head = temp->next;
    }
    else
    {
        prev->next = temp->next;
    }

    free(temp);

    printf("Element %d deleted successfully.\n", value);
}

void display(struct Node *head)
{
    struct Node *temp = head;

    while (temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }
}

int main()
{
    struct Node *head = NULL;
    struct Node *newNode;
    struct Node *temp;
int n, i, value;

printf("Enter the number of nodes: ");
scanf("%d", &n);

for (i = 0; i < n; i++)
{
    newNode = (struct Node *)malloc(sizeof(struct Node));

    printf("Enter element %d: ", i + 1);
    scanf("%d", &newNode->data);

    newNode->next = NULL;

    if (head == NULL)
    {
        head = newNode;
    }
    else
    {
        temp = head;

        while (temp->next != NULL)
        {
            temp = temp->next;
        }

        temp->next = newNode;
    }
}

printf("\nLinked list before deletion:\n");
display(head);

printf("\n\nEnter the element to delete: ");
scanf("%d", &value);

deleteElement(&head, value);

printf("\nLinked list after deletion:\n");
display(head);

return 0;
}
```

Output:

<img width="848" height="522" alt="image" src="https://github.com/user-attachments/assets/e5e43c83-9c24-4d2a-8d08-dc31c21fcb5d" />






Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





