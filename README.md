# 635314
Tìm cách chèn phần tử a[i] vào vị trí thích hợp của đoạn đã được sắp để có dãy mới a[0] , a[1] ,... , a[i-1] trở nên có thứ tự Vị trí này chính là pos thỏa : a[pos-1] &lt;= a[i ]&lt; a[pos] (1 &lt;= pos &lt;= i)
void InsertionSort(int a[], int n){	
	int pos, x;
	for(int i = 1; i < n; i++){ //đoạn a[0] đã sắp
		x = a[i]; 
		pos = i;
		while(pos > 0 && x < a[pos-1]){
			a[pos] = a[pos-1];	// dời chỗ
			pos--;
		}
		a[pos] = x;
	}
}
