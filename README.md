This project finds the common friends from a given data set.

The input for mapper is
<UserID!><,><FriendID!><space><FriendID!>…< FriendID!>
Ex: 101,102 103 104 105 106
The output of mapper is in the format of <key, value> pair
Here key will be <UserID!>,<FriendID!> if userid is greater than friend id else <FriendID!>, <UserID!>
And value is the list of all the friends for the user <FriendID!><space><FriendID!>…< FriendID!>
Ex:
Output is
101,102<tab>102 103 104 105 106
101,103<tab>102 103 104 105 106
101,104<tab>102 103 104 105 106
101,105<tab>102 103 104 105 106
101,106<tab>102 103 104 105 106
For the input 101,102 103 104 105 106
The input for reducer is
The output of mapper . i.e. <101,102<tab>102 103 104 105 106 >
The output of reducer is
<UserID!><,><UserID!><space><[><FriendID!><,><FriendID!>….< FriendID!><]>
Ex: 101,102 [103,104]
