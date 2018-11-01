# fuelefficiency
#include <iostream>
using namespace std;


class Odometer
//the main class
{
private:
    double miles;
    //miles to sum gallons
    double fuel_efficiency;
    //fuel efficiency to calculate

public:
    //constractor
    Odometer()
    {
        miles = 0.0;
        fuel_efficiency = 0.0;
    }

    void reset()
    {
        //function to reset odmeter
        miles = 0.0;
        //fuel_efficiency = 0.0;
    }

    void setFuelEfficiency(double Fuel_efficiency)
    {
        //to sum fuel efficiency
        fuel_efficiency = Fuel_efficiency;
    }

    void milesdriven(double Miles)
    {
        //to calculate all of miles driven
        miles += Miles;
    }

    double gallonofgas()
    {
        //calculate the gallons that have been consumed
        return miles/fuel_efficiency;
    }



};


int main()
{

    Odometer trip1, trip2 , trip3;
    //3 objects to 3 cases
    trip1.reset();
    trip1.setFuelEfficiency(50);
    //to set fuel efficiency
    trip1.milesdriven(100);
    //to input miles driven
    cout << "For your fuel-efficient small car:" << endl;
    cout << "After 100 miles, " << trip1.gallonofgas() <<
         " gallons were used." << endl;
    trip1.milesdriven(50);
    cout << "After another 50 miles, " << trip1.gallonofgas() <<
         " gallons were used." << endl;

    cout <<"------------------------------------------------"<< endl;

    trip2.reset();
    trip2.setFuelEfficiency(25);
    trip2.milesdriven(100);
    cout << "For your gas guzzler:" << endl;
    cout << "After 100 miles, " << trip2.gallonofgas() <<
         " gallons were used." << endl;
    trip2.milesdriven(150);
    cout << "After another 150 miles, " << trip2.gallonofgas() <<
         " gallons were used." << endl;

    cout<<"-------------------------------------"<<endl;
    trip2.reset();
    trip2.setFuelEfficiency(20);
    trip2.milesdriven(100);
    cout << "For your gas guzzler:" << endl;
    cout << "After 100 miles, " << trip2.gallonofgas() <<
         " gallons were used." << endl;
    trip2.milesdriven(40);
    cout << "After another 40 miles, " << trip2.gallonofgas() <<
         " gallons were used." << endl;

    return 0;
}
