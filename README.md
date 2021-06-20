# Game
Board
#ifndef Board_H
#define Board_H
#include<string>
#include<exception>
using namespace std;
 Board::Board(int size) : n_Size(size)
 {
     n_Board = new Figure**[size];
     for (int i=0; i<size; i++)
     {
         n_Board[i] = new Figure*[size];
         for (int j=0; j<size; j++) 
         {
             n_Board[i][j] = nullptr;
         }
     }
     int lines = size / 2 - 1;
     for (int i=0; i<lines; i++) 
     {
         for (int j = i%2; j<size; j+=2)
         {
             n_Board[i][j] = new Checker (this,i,j,Color::White)
         }
     }
 }
 Board::Board() 
 {
     
 }
 Board::Board(const Board& other) 
 {
     
 }
 Board& Board(const Board& other) 
 {
     f (this == &rhs) return *this; 
    return *this;
 }
