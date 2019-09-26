#include <stdio.h>
#include <stdlib.h>

struct cvor
{
  int val;
  struct cvor *p;

};

void dodaj(struct cvor **lista, int val)
{
    struct cvor *nc=(struct cvor*)malloc(sizeof(struct cvor));
    nc->val=val;
    nc->p=*lista;
    *lista=nc;

};

void ispis(struct cvor *lista)
{
    while(lista)
    {
        printf("%d ",lista->val);
        lista=lista->p;
    }
}


int main()
{
  int n,m,x,y;
  scanf("%d%d",&n,&m);
  struct cvor **lista = (struct cvor *)calloc(n, sizeof(struct cvor *));

  for(int i=0; i<m; i++)
  {
    scanf("%d%d",&x,&y); //Usmeren bestezinski graf
    dodaj(&lista[x],y);
  }

  for(int i=0; i<n; i++)
  {
     printf("Susedi od cvora %d: ", i);
     ispis(lista[i]);
     putchar('\n');
  }
}
