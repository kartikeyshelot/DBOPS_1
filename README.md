{
  "sqlStatement": "SELECT
    timeInterval_Month AS Month,
    aws_dimension_InstanceId AS Instance_ID,
    aws_dimension_Region AS Region,
    aws_dimension_InstanceType AS Instance_Type,
    SUM(aws_measure_UnblendedCost) AS Cost
  FROM
    AWS_CUR
  GROUP BY
    timeInterval_Month,
    aws_dimension_InstanceId,
    aws_dimension_Region,
    aws_dimension_InstanceType",
  "needBackLinkingForTags": true,
  "dataGranularity": "MONTHLY",
  "timeRange": {
    "last": 1
  },
  "limit": -1
}
