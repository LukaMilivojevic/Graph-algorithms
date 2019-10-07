#include <stdio.h>
#include <iostream>
#include <stdlib.h>
#include <list>
#include <iterator>
using namespace std;
void display_list(list<int> adj_list[], int v){
    for(int i = 0; i<v; i++) {
      cout << i << "--->";
      list<int> :: iterator it;
      for(it=adj_list[i].begin(); it!=adj_list[i].end(); ++it){
        cout << *it << " ";
     }
     cout << endl;
   }
}

void add_edge(list<int> adj_list[],int a, int b){
    adj_list[a].push_back(b);
    adj_list[b].push_back(a);
}
int main()
{
 int u,v,a,b;
 cout << "Unesi broj cvorova: ";
 cin >> v;
 list<int> lista[v];
 cout << "Unesi broj grana: ";
 cin >> u;
 for(int i=0; i<u; i++ ){
  cin >> a;
  cin >> b;
  add_edge(lista, a, b);
 }
 display_list(lista,v);
 int brojac=0;
 int niz[v];
 
 list<int> :: iterator it;
for(int i = 0; i<v; i++) {
 for(it=lista[i].begin(); it!=lista[i].end(); ++it){
         brojac++;
 }
  niz[i]=brojac;
  brojac=0;
}
for(int i=0; i<v; i++ ){
    cout << (niz[i]);
}
}
