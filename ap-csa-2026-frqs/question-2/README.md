public class Bottle
{
    private double capacity;
    private double amountRemaining;

    public Bottle(double bottleCapacity)
    {
        capacity = bottleCapacity;
        amountRemaining = bottleCapacity;
    }
    public double updateAmount(double amountToRemove)
    {
        amountRemaining -= amountToRemove;
        
        if (amountRemaining < (0.25 * capacity))
        {
            amountRemaining = capacity;
        }
        
        return amountRemaining;
    }
}
