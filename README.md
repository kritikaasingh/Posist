
#include<bits/stdc++.h>
using namespace std;

struct data   //structure for data of node
{
	int ownerId;
	float value;
	string ownerName;
	map<int,float,string> m;
}

struct node  //structure of node
{
	int *parent=NULL;
	int *child1=NULL;
	int *child2=NULL:
	int date;
	struct data;
	int nodeNumber;
	string nodeId;
	string referenceNodeId;
	string childReferenceNOdeId;
	string genesisReferenceNodeId;
	;
}

node genesis=new node;
genesis->parent=NULL;
genesis->child1=NULL;
genesis->child2=NULL;

void insertnode(struct genesis,struct n)  //insert node at right position
{
	if(genesis->date==NULL)
	   genesis=n;
	   
    else if(genesis->child1==NULL)
       child1=n;
       
    else if(genesis->child2==NULL)
       child2=n;
       
    else
	{
    	insertnode(genesis->child1,n);
    	insertnode(genesis->child2,n);
	}
}

void insertdata()  //insert data for the new node
{
	cout<<"";
	node n=new node;
	cin>>n->date;
	data d=new data;
	cin>>n->d->ownerId>>n->d->value>>n->d->ownerName>>n->d->m;
	insertnode(genesis,n); // call function to place the new node n at right position
}

void findLongestChainfromRoot(struct genesis)
{

}

void findLongestChain(struct genesis)
{

}

void merge(int id1, int id2)
{

}


int main()
{
     
     cout<<"Menu:"<<endl;  ////menu driven user functionality listing to chose from
     cout<<"1. Insert Node";
     cout<<"2. Longest Chain from Root"<<endl;
     cout<"3. Longest Chain"<<endl;
     cout<<"4. Merge"<<endl;
     cout<<"5. Exit"<<endl;
     
     int c;   //input of the choice of the user
     cin>>c;
     
	 switch(c)
	 {
	 	case'1':
	 		{
			 	insertdata(); //if user selects to insert data then call the insert function
	 		    break;
			}
		case '2':
			{
				findLongestChainfromRoot(genesis);   //this would search for the longest chain starting from the genesis root in left or right direction
        break;
			}
	 	case '3':
      {
          findLongestChain(genesis);   //this would find the longest chain from left to right most node of the tree
          break;
      }
    case '4':
      {
          cout<<"Input nodeId of nodes to merge"; 
          int id1,id2;
          cin>>id1>>id2;
          merge(node1,node2); //search the tree using the nodeId and then facilitate merging
          break;
      }
    case '5':
      {
         return 0;
      }
   default:
     {
         return 0;
     }
	 			
	 }	
}
