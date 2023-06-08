# CreationalDesignPattersDemo
A project developed to show the Creational Design Patters i learned at Uni.

The Singleton Pattern is used in the Controller class to ensure that only one instance of the Controller class is created, and is referenced in the Instance getter property. This is useful in this code because the Controller script is applied to every object in the scene, which would create multiple instances of the script and likely lead to code confusion. By using the Singleton pattern, only one instance of the Controller is created and this instance is referenced by the Instance property.

Code example for Singleton Pattern:

private static Controller instance = null;
public static Controller Instance
{
    get
    {
        if (instance == null)
        {
            instance = new Controller();
        }
        return instance;
    }


The FactoryMethod is used to instantiate the TransmitterProxy object. Instead of directly instantiating the object using the "new" keyword, the FactoryMethod is used to instantiate an object referred to as a "go" object, and then assign the TransmitterProxy object reference to this object. This helps keep the code organized and allows for the creation of multiple instances of the TransmitterProxy class, if needed. The FactoryMethod also allows for the reusability of code by moving the object instantiation outside of the code.

Code example for FactoryMethod:

public class TransmitterProxy
{
    public static TransmitterProxy Create()
    {
        GameObject go = new GameObject();
        return go.AddComponent<TransmitterProxy>();
    }
    
    // TransmitterProxy methods and properties
}

:see_no_evil: :hear_no_evil: :speak_no_evil:
