

#include <iostream>
#include <string>

using namespace std;

String divide(String s)
{
    int i,j;
    char x;
    String div = "10001000000100001";
    for(i=0;i<7;i++)
    {
        x = s[i];
        for(j=0;j<17;j++)
        {
            if(x=='1'){
                if(s[i+j]!=div[j]){
                    s = s.substr(0,i+j) + "1" + s.substr(i+j+1);
                }
                else{
                    s = s.substr(0,i+j) + "0" + s.substr(i+j+1);
                }
            }
        }
    }
    return s;
}
int main()
{
    int n;
    int choice;
    int errorPos;
    long data = 0;
    std::string divisor = "10001000000100001";
    std::string zero = "0000000000000000";
    std::string code,copy;
    cout<<"CRC 16-bit";
    cout<<"\nEnter the data(dividend)";
    cin>>code;
    cout<<"\nStandard polynomial(divisor/g(x)) is 10001000000100001";
    n = code.length();
    copy = code;
    code = code+zero;
    cout<<"\nModified data is"<<code;
    code = divide(code);
    cout<<"\nChecksum is "<<code.substr(n);
    cout<<"\nFinal codeword is "<<copy;
    cout<<"\nError checking 1(yes) 2(no)";
    cin>>choice;
    if(choice==1){
    cout<<"\nEnter error position: ";
    cin>>errorPos;
    if(copy[errorPos]=='1')
    {
        copy = copy.substr(0,errorPos) + "0" + copy.substr(errorPos+1);
    }
    else
    {
        copy = copy.substr(0,errorPos) + "1" + copy.substr(errorPos+1);
    }
    cout<<"\nData causing error"<<copy;
    cout<<"\nError detected";
    }
    else{
        cout<<"\nNo error found";
    }
    return 0;
}
