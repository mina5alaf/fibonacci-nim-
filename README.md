# fibonacci-nim-
 cout<<"\t"<<"\t"<<"\t"<<"\t"<<"\t"<<"welcome to fibonacci nim game"<<endl;
    string choice;
    cout<<"one player or two player : ";
    cin>>choice;
    cin.ignore();
    cin>>choice;
    if (choice=="two player")
    {
        string player_1,player_2;
        cout<<"enter the first player name : ";
        cin>>player_1;
        cout<<"enter the second player name : ";
        cin>>player_2;
        cout<<endl;

        int coins_num,num_1,num_2;
        cout<<"enter the number of coins :";
        cin>>coins_num;
        cout<<endl;
        for (int i =0; i<=(coins_num*10); i++)
        {
            bool p=true;
            cout<<"enter the number of coins taken by player 1 :";
            cin>>num_1;
            while (p)
            {
                if (num_1>coins_num || num_1>num_2*2)
                {
                    cout<<"invalid number"<<"\n";
                    cout<<"enter the number of coins taken by player 1 :";
                    cin>>num_1;

                }
                else
                {
                    p=false;
                }

            }
            coins_num-=num_1;
            if (coins_num<=0)
            {
                cout<<player_1<<" YOU WIN"<<"\n";
                break;
            }
            bool c=true;
            cout<<"enter the number of coins taken by player 2 :";
            cin>>num_2;
            while (c)
            {
                if (num_2>num_1*2 || num_2>coins_num)
                {
                    cout<<"invalid number"<<"\n";
                    cout<<"enter the number of coins taken by player 2 :";
                    cin>>num_2;
                }
                else
                    c=false;

            }
            coins_num-=num_2;
            if (coins_num<=0)
            {
                cout<<player_2<<" YOU WIN"<<"\n";
                break;
            }
        }

    }
    else
    {
        string player;
        int coins_num,num,num2;
        cout<<"Enter the player name : ";
        cin>>player;
        cout<<endl;
        cout<<"enter the number of coins : ";
        cin>>coins_num;
        cout<<endl;
        for (int i =0; i<=(coins_num*10); i++)
        {
            bool p=true;
            cout<<"enter the number of coins taken by the player  :";
            cin>>num;
            while (p)
            {
                if (num>coins_num || num>((2*num2)-1)*2)
                {
                    cout<<"invalid number"<<"\n";
                    cout<<"enter the number of coins taken by the player :";
                    cin>>num;

                }
                else
                {
                    p=false;
                }

            }
            coins_num-=num;
            if (coins_num=0)
            {
                cout<<player<<" YOU WIN"<<"\n";
                break;
            }
            if (num==1)
            {
                cout<<"number of coins taken by the com : "<<2<<"\n";
                coins_num-=2;
            }
            else
            {
                cout<<"number of coins taken by the com : "<<((2*num)-1)<<"\n";
                coins_num-=((2*num)-1);
            }

            if (coins_num<=0)
            {
                cout<<player<<" YOU LOSE"<<"\n";
                break;
            }
        }
    }
