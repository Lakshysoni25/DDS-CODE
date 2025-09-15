#include<iostream>
using namespace std;

struct Node 
{
    int data;
    Node * left;
    Node * right;
    Node (int val)
    {
        data = val;
        left=right=nullptr;
    }
};

Node * insert(Node*root,int val)
{
 if(root==nullptr)
 {
     return new Node(val);
 }
 else if(val<root->data)
 {
     root->left = insert (root->left,val);
 }
 else if(val>root->data)
 {
     root->right = insert(root->right,val);
 }
 return root;
}

void inorder(Node*root)
{
    if(root)
    {
        inorder(root->left);
        cout<<root->data<<"  ";
        inorder(root->right);
    }
}

int main()
{
    int n;
    cout<<"Enter no. of Nodes : ";
    cin>>n;
    
    int*arr = new int[n];
    for(int i=0;i<n;i++)
    {
        cin>>arr[i];
    }
    Node*root =nullptr;
    for( int i=0;i<n;i++)
    {
        root = insert(root,arr[i]);
    }
    cout<<endl;
    inorder(root);
}
