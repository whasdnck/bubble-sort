# bubble-sort

### 서로 인접한 두 원소를 검사하여 정렬하는 알고리즘
### 인접한 2개의 레코드를 비교하여 크기가 순서대로 되어 있지 않으면 서로 교환한다.
### 선택 정렬과 기본 개념이 유사하다.


# 버블 정렬(bubble sort) 알고리즘의 구체적인 개념

### 1회전을 수행하고 나면 가장 큰 자료가 맨 뒤로 이동하므로 2회전에서는 맨 끝에 있는 자료는 정렬에서 제외되고,
### 2회전을 수행하고 나면 끝에서 두 번째 자료까지는 정렬에서 제외된다.
### 이렇게 정렬을 1회전 수행할 때마다 정렬에서 제외되는 데이터가 하나씩 늘어난다.

# 버블 정렬(bubble sort) c언어 코드

void bubbleSort(int* arr){
    int i,j, temp;
    for(i=0; i < LEN; i++){
        for(j=0; j<LEN-i-1; j++){
            if(arr[j] > arr[j+1]){    // swap
                temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
            }
        }
    }
}
 
int main(){
    int arr[LEN] = {7,5,1,4,3};
    int i;
    printf("정렬 전 : ");
    for(i=0; i<5; i++){
        printf("%d ", arr[i]);
    }
    printf("\n");
    
    bubbleSort(arr);
    printf("정렬 후 : ");
    for(i=0; i<5; i++){
        printf("%d ", arr[i]);
    }
    printf("\n");    
    
    return 0; 
}
