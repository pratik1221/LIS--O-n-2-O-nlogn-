# LIS--O-n-2-O-nlogn-

O(n^2)
 ll LIS(ll a[],ll n)
  {
      ll lis[n];
      f(i,0,n)
      lis[i]=1;
      vector<ll>v;
      f(i,0,n)
      {
        f(j,1+i,n)
        {
          if(a[j]>a[i]&&lis[j]>=lis[i])
          lis[j]=1+lis[i];
          v.pb(lis[j]);

        }
      }
      sort(v.begin(),v.end());
      return v[v.size()-1];
  }
.
.
.
O(nlogn)
ll LIS(ll a[],ll n)
  {
     vector<ll>v;
     v.pb(a[0]);
     f(i,1,n)
     {
       if(v.back<a[i])
       v.pb(a[i]);
       else
       {
         ll idx=ub(v.begin(),v.end(),a[i])-v.begin();
         v[idx]=arr[i];
       }
     }
       return v.size();
  }
                       
                       
                       NON_DECREASING SUBSEQUENCE
                       
                       
                       
  ll LIS(ll a[],ll n)
  {
     vector<ll>v;
     v.pb(a[0]);
     f(i,1,n)
     {
       if(v.back<=a[i])     //less than equal to
       v.pb(a[i]);
       else
       {
         ll idx=ub(v.begin(),v.end(),a[i])-v.begin();   //upper_bound
         v[idx]=arr[i];
       }
     }
       return v.size();
  }


                       
                       
                       

