public int moreHistoryThanMathAbsences()
{
    int matchCount = 0;

    for (int h = 0; h < historyList.size(); h++)
    {
        CourseRecord historyRecord = historyList.get(h);
        String historyID = historyRecord.getStudentID();

        for (int m = 0; m < mathList.size(); m++)
        {
            CourseRecord mathRecord = mathList.get(m);
            
            if (historyID.equals(mathRecord.getStudentID()))
            {
                if (historyRecord.getAbsences() > mathRecord.getAbsences())
                {
                    matchCount++;
                }
            }
        }
    }

    return matchCount;
}
