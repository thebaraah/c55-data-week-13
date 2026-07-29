# AI Usage Log

Record at least one point where you used an AI coding assistant (ChatGPT, Claude, Cursor, GitHub Copilot, Gemini, etc.) during this assignment.

## Interaction 1

- **Tool used:** Claude
- **Task / Problem:** Debugging PySpark Task 1 aggregation and understanding Spark transformations
- **Prompt sent:**
  > I am working on a Databricks PySpark task. I need to join `hyf.nyc_yellow.raw_trips` with `hyf.nyc_yellow.raw_zones` to find which pickup borough has the most trips and calculate the average `total_amount` per `payment_type`. Help me check my transformation chain and explain why we use `show()` instead of `collect()`.

- **Output provided by AI:**
  > The AI explained that the join is needed because `pickup_location_id` is only an ID, while `raw_zones` contains the readable borough names. It also explained that `groupBy()` and `agg()` are transformations, while `show()` is an action that triggers Spark execution. 
  It suggested checking the aggregation code and using `F.avg("total_amount").alias("avg_total_amount")` to create the required output column.
- **What I kept, changed, or rejected, and why:**
  > I kept the explanation of Spark transformations and actions because it helped me understand the execution model. I changed my code by fixing the aggregation step and adding the correct alias for the average column. I verified the final code by running it in Databricks and checking the output with `show()`.

*(Ensure no personal passwords, Databricks tokens, or unapproved credentials are included in prompts or logged outputs.)*
