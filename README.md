## tic-tac-toe-program
#include<iostream>
using namespace std;
void showboard()
    { 
     for (int i=0; i<3; i++) 
    { 
        for (int j=0; j<3; j++) 
        {   int board[i][j] = ' ';
            cout<<board[i][j];  }
    } }
    
void turn()
    { 
      cout<<"choose cells from the matrix "<<endl;
      showboard();
      for(i=0;i<3;i++)
      {
          for(j=0;j<3;j++)
          cin>>input[i][j];
      if(input[i][j]==1||input[i][j]==2||input[i][j]==3||input[i][j]==4||input[i][j]==5||input[i][j]==6||input[i][j]==7||input[i][j]==8||input[i][j]==9)
      {   if(input[i][j]=1)
          {
            comp++;
            board[1][2]==input[i][j];
            rowcross();
            colcross();
            diagcross();
            computerboard[0][0]==comp;
            rowcompcross();
            colcompcross();
            diagcompcross();
          else if(input[i][j]=9)
            comp--;
          else
            comp+=input[i][j];
      }
      else
      cout<<"wrong choice";
    }
    
void win()
    {if(turn==user)
    cout<<"user has won";
    else
    cout<<"computer has won";
    }
    
void rowcross()
    {
     for (i=0; i<size; i++) 
    { 
        if (board[i][0] != ' ')
        cout<<win();
    } 
    else
        cout<<turn();
    }
    
void rowcompcross()
    {
     for (i=0; i<size; i++) 
    { 
        if (computerboard[i][0] != ' ')
        cout<<win();
    } 
    else
        cout<<turn();
    }    
    
void colcross() 
   { 
    for (int i=0; i<size; i++) 
    { 
        if (board[0][i] != ' ') 
            cout<<win();; 
    } 
    else
        cout<<turn();
} 

void colcompcross() 
   { 
    for (int i=0; i<size; i++) 
    { 
        if (computerboard[0][i] != ' ') 
            cout<<win();; 
    } 
    else
        cout<<turn();
}

void diagcross() 
   { 
    if (board[0][0] != ' ') 
        cout<<win(); 
          
    else if (board[0][2] != ' ') 
        cout<<win(); 
    else
        cout<<turn(); 
} 


void diagcompcross() 
   { 
    if (computerboard[0][0] != ' ') 
        cout<<win(); 
          
    else if (computerboard[0][2] != ' ') 
        cout<<win(); 
    else
        cout<<turn(); 
} 

int main() 
{
    int user,comp=0;
   int size=3, i, j, input[3][3], board[3][3], computerboard[3][3];
   int b[3][3] = { {2,7,6} , {9,5,1} , {4,3,1} };
   cout<<"The matrix is:"<<endl;
   for(i=0; i<3; ++i) {
      for(j=0; j<3; j++)
      cout<<b[i][j]<<" ";
      cout<<endl;
   }
    cout<<endl;
    cout<<"the first turn is of user, computer will occupy its place accordingly =";
    turn();
    return 0;
}
       return 0;
   }
   
