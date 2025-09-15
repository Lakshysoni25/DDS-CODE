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

Node * insert(Node*root,int arr[],int i,int n)
{
    if(i<n)
    {
        Node*temp = new Node(arr[i]);
        root = temp;
        root->left = insert(root->left,arr,2*i+1,n);
        root->right = insert(root->right,arr,2*i+2,n);
    }
    return root;
}

void inorder(Node*root)
{
    if(root)
    {
        inorder(root->left);
        cout<<root->data;
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
    Node*root = nullptr;
    root = insert(root,arr,0,n);
    
}
