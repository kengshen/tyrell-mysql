1. Make sure to have unique index on all the many-to-many table
 - jobs_personalities (job_id, personality_id)
 - jobs_practical_skills (job_id, practical_skill_id)
 - jobs_basic_abilities (job_id, basic_ability_id)
 - affiliates (job_id, affiliate_id)
 - jobs_rec_qualifications (job_id, affiliate_id)

2. Make sure to have index on "sort_order" column in jobs table as it was used for ordering

3. Avoid duplicate query on line below
 - LEFT JOIN jobs_req_qualifications JobsReqQualifications
 - LEFT JOIN affiliates ReqQualifications
 
4. Explain the query and see if the indexes were used

5. If all the above doesn't help / meet the performance improvement. Try reviewing the requirement again, and see if all the data are required to be returned, and/or all the table joining is necessary, else remove when possible.
