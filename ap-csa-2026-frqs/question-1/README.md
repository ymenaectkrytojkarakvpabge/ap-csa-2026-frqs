public Account(String requestedName)
{
    if (isAvailable(requestedName))
    {
        username = requestedName;
    }
    else
    {
        int count = 1;
        while (!isAvailable(requestedName + count))
        {
            count++;
        }
        username = requestedName + count;
    }
}
public String getShortenedName()
{
    String result = "";
    int i = 0;
    
    while (i < username.length())
    {
        // Check if the NEXT character is a hyphen.
        // If it is, skip both the current character and the hyphen.
        if (i + 1 < username.length() && username.substring(i + 1, i + 2).equals("-"))
        {
            i += 2; 
        }
        else
        {
            result += username.substring(i, i + 1);
            i++;
        }
    }
    
    return result;
}
