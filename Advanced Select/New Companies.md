계층 : Founder -> Lead Manager->Senior Manager-> Manager->Employee
테이블 : Company, Lead Manager, Senior Manager, Manager, Employee
각 테이블마다 company code 존재
- 출력 : company_code, founder name,total number of lead managers, total number of senior_managers, total number of managers, and total number of employees.
- 정렬 : company_code
	- For example, if the _company_codes_ are _C_1_, _C_2_, and _C_10_, then the ascending _company_codes_ will be _C_1_, _C_10_, and _C_2_.
- 중복 있어도 됨

SELECT C.company_code <br/>
            ,C.founder<br/>
            ,COUNT(DISTINCT E.lead_manager_code)<br/>
            ,COUNT(DISTINCT E.senior_manager_code)<br/>
            ,COUNT(DISTINCT E.manager_code)<br/>
            ,COUNT(DISTINCT E.employee_code)<br/>
FROM Company AS C<br/>
            INNER JOIN Employee AS E ON C.company_code=E.company_code<br/>
GROUP BY C.company_code,C.Founder<br/>
ORDER BY C.Company_code