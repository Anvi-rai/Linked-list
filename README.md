# Linked-list
Each function (create_first, Add_Node, display) plays a role in constructing and displaying the linked list.
#include<iostream>
#include<stdlib.h>

using namespace std;

struct Node
{
	int data;
	Node *next;
	
};
 Node *first, *temp, *ttemp;
void create_first(int value)
{
	first=(Node*)malloc(sizeof(Node));
	first->data=value;
	first->next=NULL;
}
void Add_Node(int value)
{
	temp=first;
	while (temp->next!=NULL)
	{
		temp=temp->next;
	}
	ttemp=(Node*)malloc(sizeof(Node));
	ttemp->data=value;
	ttemp->next=NULL;
	temp->next=temp;
}
void display()
{
	temp=first;
	while(temp!=NULL)
	{
		cout<<temp->next;
		temp=temp->next;
	}
}
int main() {
    int n;  // Declare n
    cout << "Enter the first value: ";
    cin >> n;
    create_first(n);
    // Continue with the rest of the code...
}
