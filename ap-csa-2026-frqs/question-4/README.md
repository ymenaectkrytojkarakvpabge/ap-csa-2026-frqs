public int getPointsForRow(int targetRow)
{
    int sum = 0;
    boolean allSameColor = true;
    
    String baseColor = board[targetRow][0].getColor();
    
    for (int col = 0; col < board[targetRow].length; col++)
    {
        sum += board[targetRow][col].getPoints();
        
        if (!board[targetRow][col].getColor().equals(baseColor))
        {
            allSameColor = false;
        }
    }
    
    if (allSameColor)
    {
        return 2 * sum;
    }
    else
    {
        return sum;
    }
}
