#include<bits/stdc++.h>
using namespace std;
const int N=3;
char **U,**D,**F,**B,**R,**L;

void swap(char *a,char *b){
	char t=*a;
	*a=*b; *b=t;
}

void swap4(char *p,char *q,char *r,char *s){	
	char t=*s;
	*s=*r; *r=*q;
	*q=*p; *p=t;		
}

void transpose1(char **M){	
	for(int i=0;i<N;i++)
		for(int j=i+1;j<N;j++)
			swap(&M[i][j],&M[j][i]);
}

void transpose2(char **M){
	for(int i=0;i<N;i++)
		for(int j=0;j<N-1-i;j++)
			swap(&M[i][j],&M[N-1-j][N-1-i]);
}

void reverse(char **M){	
	for(int i=0;i<N;i++)
		for(int j=0;j<N/2;j++)
			swap(&M[i][j],&M[i][N-1-j]);
}

void rotate_clock(char **M){
	transpose1(M);
	reverse(M);
}

void rotate_anticlock(char **M){
	transpose2(M);
	reverse(M);
}

void turn_right(){
	rotate_clock(U);
	rotate_anticlock(D);
	for(int i=0;i<N;i++)
		for(int j=0;j<N;j++)
			swap4(&F[i][j],&L[i][j],&B[i][j],&R[i][j]);
	cout<<"Turn_right-";
}

void turn_left(){
	rotate_anticlock(U);
	rotate_clock(D);
	for(int i=0;i<N;i++)
		for(int j=0;j<N;j++)
			swap4(&R[i][j],&B[i][j],&L[i][j],&F[i][j]);
	cout<<"Turn_left-";
}

void up(){
	rotate_clock(U);
	for(int i=0;i<N;i++)
		swap4(&F[0][i],&L[0][i],&B[0][i],&R[0][i]);
	cout<<"Up-";
}

void upi(){
	rotate_anticlock(U);
	for(int i=0;i<N;i++)
		swap4(&R[0][i],&B[0][i],&L[0][i],&F[0][i]);
	cout<<"Upi-";
}

void middle(){
	for(int i=0;i<N;i++)
		swap4(&F[1][i],&L[1][i],&B[1][i],&R[1][i]);
	cout<<"Middle-";
}

void middlei(){
	for(int i=0;i<N;i++)
		swap4(&R[1][i],&B[1][i],&L[1][i],&F[1][i]);
	cout<<"Middlei-";
}

void down(){
	rotate_clock(D);
	for(int i=0;i<N;i++)
		swap4(&R[N-1][i],&B[N-1][i],&L[N-1][i],&F[N-1][i]);
	cout<<"Down-";
}

void downi(){
	rotate_anticlock(D);
	for(int i=0;i<N;i++)
		swap4(&F[N-1][i],&L[N-1][i],&B[N-1][i],&R[N-1][i]);
	cout<<"Downi-";
}

void front(){
	rotate_clock(F);
	for(int i=0;i<N;i++)
		swap4(&U[N-1][i],&R[i][0],&D[0][N-1-i],&L[N-1-i][N-1]);
	cout<<"Front-";
}

void fronti(){
	rotate_anticlock(F);
	for(int i=0;i<N;i++)
		swap4(&L[N-1-i][N-1],&D[0][N-1-i],&R[i][0],&U[N-1][i]);
	cout<<"Fronti-";
}

void back(){
	rotate_clock(B);
	for(int i=0;i<N;i++)
		swap4(&L[N-1-i][0],&D[N-1][N-1-i],&R[i][N-1],&U[0][i]);
	cout<<"Back-";	
}

void backi(){
	rotate_anticlock(B);
	for(int i=0;i<N;i++)
		swap4(&U[0][i],&R[i][N-1],&D[N-1][N-1-i],&L[N-1-i][0]);
	cout<<"Backi-";
}

void right(){
	rotate_clock(R);
	for(int i=0;i<N;i++)
		swap4(&U[i][N-1],&B[N-1-i][0],&D[i][N-1],&F[i][N-1]);
	cout<<"Right-";
}

void righti(){
	rotate_anticlock(R);
	for(int i=0;i<N;i++)
		swap4(&F[i][N-1],&D[i][N-1],&B[N-1-i][0],&U[i][N-1]);
	cout<<"Righti-";
}

void left(){
	rotate_clock(L);
	for(int i=0;i<N;i++)
		swap4(&F[i][0],&D[i][0],&B[N-1-i][N-1],&U[i][0]);
	cout<<"Left-";
}

void lefti(){
	rotate_anticlock(L);
	for(int i=0;i<N;i++)
		swap4(&U[i][0],&B[N-1-i][N-1],&D[i][0],&F[i][0]);
	cout<<"Lefti-";
}

void RiDiRD(){
	righti();downi();right();down();
}

void FiUiFU(){
	fronti();upi();front();up();
}

void URUiRiUiFiUF(){
	up();right();upi();righti();upi();fronti();up();front();
}

void UiLiULUFUiFi(){
	upi();lefti();up();left();up();front();upi();fronti();
}

void FRURiUiFi(){
	front();right();up();righti();upi();fronti();
}

void RURiURUURi(){
	right();up();righti();up();right();up();up();righti();
}

void URUiLiURiUiL(){
	up();right();upi();lefti();up();righti();upi();left();
}

char** in(){
	char **M=new char* [N];
	for(int i=0;i<N;i++)
		M[i]=new char[N];
	for(int i=0;i<N;i++)
		for(int j=0;j<N;j++)
			cin>>M[i][j];
	return M;
}

void out(char **M){
	cout<<"\n";
	for(int i=0;i<N;i++){
		for(int j=0;j<N;j++)
			cout<<M[i][j]<<" ";
		cout<<"\n";
	}
}

void print_all(){
	out(U);out(D);out(F);out(B);out(R);out(L);
}

void making_plus(){
	if(U[0][1]==D[1][1] && U[1][0]==D[1][1] && U[1][2]==D[1][1] && U[2][1]==D[1][1])
		return;
	for(int i=0;i<4;i++){
		down();
		if(D[1][2]==D[1][1]){
			while(U[1][2]==D[1][1])
				up();
			right();right();
		}	
	}
	for(int i=0;i<4;i++){
		middle();
		if(F[1][2]==D[1][1]){
			while(U[1][2]==D[1][1])
				up();
			right();
		}	
	}		
	for(int i=0;i<4;i++){
		middle();
		if(F[1][0]==D[1][1]){
			while(U[1][0]==D[1][1])
				up();
			lefti();
		}	
	}
	for(int i=0;i<4;i++){
		up();downi();
		if(F[0][1]==D[1][1] || F[2][1]==D[1][1]){
			while(U[2][1]==D[1][1])
				up();
			front();
			break;
		}
	}
	making_plus();	
}

void final_plus(){
	while(F[0][1]!=F[1][1] || U[2][1]!=D[1][1])
		up();
	front();front();
	while(B[0][1]!=B[1][1] || U[0][1]!=D[1][1])
		up();
	back();back();
	while(R[0][1]!=R[1][1] || U[1][2]!=D[1][1])
		up();
	right();right();
	while(L[0][1]!=L[1][1] || U[1][0]!=D[1][1])
		up();
	left();left();
}

bool corner_check(char *p,char *q,char *r,char *a,char *b,char *c){
	int t[26]={};
	t[*p-65]=t[*q-65]=t[*r-65]=1;
	if(t[*a-65]==1 && t[*b-65]==1 && t[*c-65]==1)
		return true;
	return false;
}

void corner_fit(){
	for(int i=0;i<4;i++){
		if(D[0][2]==D[1][1] || F[2][2]==D[1][1] || R[2][0]==D[1][1]){
			while(U[2][2]==D[1][1] || F[0][2]==D[1][1] || R[0][0]==D[1][1])
				up();
			FiUiFU();		
		}
		turn_right();
	}
	for(int i=0;i<4;i++){
		while(!corner_check(&U[2][2],&F[0][2],&R[0][0],&D[1][1],&F[1][1],&R[1][1]))
				up();
		while(D[1][1]!=D[0][2] || F[1][1]!=F[2][2] || R[1][1]!=R[2][0] )
			FiUiFU();		
		turn_right();
	}	
}

void second_layer(){
	for(int i=0;i<4;i++){
		if(F[1][2]!=U[1][1] && R[1][0]!=U[1][1]){
			while(U[2][1]!=U[1][1] && F[0][1]!=U[1][1])
				up();
			URUiRiUiFiUF();			
		}
		turn_right();		
	}
	while(F[1][0]!=F[1][1] || F[2][0]!=F[1][1] || B[1][0]!=B[1][1] || B[2][0]!=B[1][1] ||
	      R[1][0]!=R[1][1] || R[2][0]!=R[1][1] || L[1][0]!=L[1][1] || L[2][0]!=L[1][1] ){
		for(int i=0;i<4;i++){
			if(F[0][1]==F[1][1] && U[2][1]==R[1][1])
				URUiRiUiFiUF();
			else if(F[0][1]==F[1][1] && U[2][1]==L[1][1])
				UiLiULUFUiFi();
			up();			
		}
		turn_right();		
	}
}

void upper_plus(){
	if(U[0][1]==U[1][1] && U[1][0]==U[1][1] && U[1][2]==U[1][1] && U[2][1]==U[1][1])
		return;
	for(int i=0;i<4;i++){
		if(U[1][0]==U[1][1] && U[1][2]==U[1][1]){
			FRURiUiFi();
			return;
		}
		up();	
	}
	for(int i=0;i<4;i++){
		if(U[1][0]==U[1][1] && U[2][1]!=U[1][1]){
			FRURiUiFi();FRURiUiFi();
			return;
		}
		up();
	}
	FRURiUiFi();
	upper_plus();
}

void upper_plus_final(){
	int c=0;
	while(c!=2 && c!=4){
		c=0;
		up();
		if(F[0][1]==F[1][1]) c++;
		if(B[0][1]==B[1][1]) c++;
		if(R[0][1]==R[1][1]) c++;
		if(L[0][1]==L[1][1]) c++;
	}
	if(c==4)
		return;
	for(int i=0;i<4;i++){
		if(B[0][1]==B[1][1] && R[0][1]==R[1][1]){
			RURiURUURi();up();
			return;
		}
		if(B[0][1]==B[1][1] && F[0][1]==F[1][1]){
			RURiURUURi();turn_left();
			RURiURUURi();up();			
			return;
		}
		turn_right();		
	}
}

void corner_orientation(){
	int c=0;
	for(int i=0;i<4;i++){
		if(corner_check(&U[2][2],&F[0][2],&R[0][0],&U[1][1],&F[1][1],&R[1][1]))
			c++;
		turn_right();
	}
	if(c==4)
		return;
	if(c==0)
		URUiLiURiUiL();
	for(int i=0;i<4;i++){
		if(corner_check(&U[2][2],&F[0][2],&R[0][0],&U[1][1],&F[1][1],&R[1][1]))
			break;
		turn_right();
	}
	while(!corner_check(&U[2][0],&F[0][0],&L[0][2],&U[1][1],&F[1][1],&L[1][1]))
		URUiLiURiUiL();
}

void final_fix(){
	for(int i=0;i<4;i++){
		while(U[2][2]!=U[1][1] || F[0][2]!=F[0][1] || R[0][0]!=R[0][1])
			RiDiRD();		
		upi();		
	}	
}

int main(){
	U=in();D=in();F=in();B=in();R=in();L=in();
	print_all();
	
	/*URUiLiURiUiL();RiDiRD();RURiURUURi();FRURiUiFi();UiLiULUFUiFi();URUiRiUiFiUF();FiUiFU();
	FRURiUiFi();FRURiUiFi();FiUiFU();URUiLiURiUiL();RiDiRD();RURiURUURi();FRURiUiFi();FiUiFU();
	FRURiUiFi();FRURiUiFi();FiUiFU();URUiLiURiUiL();RiDiRD();RURiURUURi();UiLiULUFUiFi();URUiRiUiFiUF();
	URUiLiURiUiL();RiDiRD();RURiURUURi();FRURiUiFi();URUiLiURiUiL();RiDiRD();RURiURUURi();FiUiFU();
	FRURiUiFi();FRURiUiFi();FiUiFU();URUiLiURiUiL();RiDiRD();RURiURUURi();FRURiUiFi();FiUiFU();
	URUiLiURiUiL();RiDiRD();RURiURUURi();FRURiUiFi();UiLiULUFUiFi();URUiRiUiFiUF();FiUiFU();*/

	print_all();
	making_plus();print_all();
	final_plus();print_all();	
	corner_fit();print_all();	
	second_layer();print_all();	
	upper_plus();print_all();	
	upper_plus_final();print_all();	
	corner_orientation();print_all();	
	final_fix();print_all();
}
