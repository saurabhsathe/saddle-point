# saddle-point



#include <iostream>
using namespace std;

int main() {
              int m[30][30],i,n,max,min=999,j,l,col,row;
              cout<<"enter the order of matrix";
              cin>>n;
              cout<<"now enter the elements of the matrix";/*1 2 3*/
                                                           /*4 5 6*/
                                                           /*7 8 9*/

              for(i=0;i<n;i++)
              {
                  for(j=0;j<n;j++)
                  {
                      cin>>m[i][j];

                  }
                  cout<<endl;
            }

             for(l=0;l<n;l++)
              {
                 max=-1;
              /*   min=m[0][0];*/
                for(i=0;i<n;i++)
                {
                          if(max<m[i][l]){
                           max=m[i][l];
                          row=i;
                          }
                }
                //cout<<"max"<<max<<endl;

                for(j=0;j<n;j++)
                                  {
                                     if(min>m[row][j]){
                                      min=m[row][j];
                                     col=j;
                                     }

                                  }
                //cout<<"min="<<min<<endl;
                  if(min==max){
                  cout<<"the saddle point is="<<m[row][col];
                          //m[row][col];
                  break;
                  }
              }
               return 0;
}
	
