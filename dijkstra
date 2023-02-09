

#include <iostream>

using namespace std;

void dijkstra(int arr[10][10],int N)
{
    int distance[N];
    int predefine[N];
    int visited[N];
    int startnode,nextnode;
    int count,min_dist;
    int i,j;
    cout<<"\nEnter the node to start with: ";
    cin>>startnode;
    for(i=0;i<N;i++)
    {
        distance[i] = arr[startnode][i];
        predefine[i] = startnode;
        visited[i] = 0;
    }
    distance[startnode] = 0;
    visited[startnode] = 1;
    count = 1;
    while(count<N-1)
    {
        min_dist = 1000;
        for(i=0;i<N;i++)
        {
            if(distance[i]<min_dist && visited[i]==0)
            {
                min_dist = distance[i];
                nextnode = i;
            }
        }
        visited[nextnode] = 1;
        for(i=0;i<N;i++)
        {
            if(visited[i] == 0)
            {
                if((min_dist + arr[nextnode][i]) < distance[i])
                {
                    distance[i] = min_dist + arr[nextnode][i];
                    predefine[i] = nextnode;
                }
            }
        }
        count = count + 1;
    }
    for(i=0;i<N;i++)
    {
        if(i!=startnode)
        {
            cout<<"\nDistance from node "<<i<<"="<<distance[i];
            cout<<"\nOptimal path is "<<i;
            j = i;
            do
            {
                j = predefine[j];
                cout<<" <- "<<j;
            }while(j!=startnode);
        }
    }
}
int main()
{
    int arr2[10][10];
    int N;
    cout<<"Dijkstra's algorithm";
    cout<<"\nEnter the number of nodes: ";
    cin>>N;
    cout<<"Enter weights/distances matrix for topology";
    for(int i = 0;i<N;i++)
    {
        for(int j = 0;j<N;j++)
        {
            cin>>arr2[i][j];
        }
    }
    dijkstra(arr2,N);
    return 0;
}


 
