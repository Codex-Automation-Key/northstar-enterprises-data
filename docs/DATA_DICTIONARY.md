# Data dictionary

Logical identifiers ending in `_id` join to the corresponding entity. Empty CSV values represent nulls; timestamps are UTC.

## business_calendar

| Column | SQLite type |
|---|---|
| `date` | TEXT |
| `weekday` | TEXT |
| `event` | TEXT |

## customer_feedback

| Column | SQLite type |
|---|---|
| `feedback_id` | TEXT |
| `ticket_id` | TEXT |
| `submitted_at` | TEXT |
| `rating` | INTEGER |
| `comment` | TEXT |

## customers

| Column | SQLite type |
|---|---|
| `customer_id` | TEXT |
| `organization_id` | TEXT |
| `email` | TEXT |
| `region` | TEXT |
| `customer_type` | TEXT |

## departments

| Column | SQLite type |
|---|---|
| `department_id` | TEXT |
| `name` | TEXT |
| `is_final_queue` | INTEGER |

## development_ingress

| Column | SQLite type |
|---|---|
| `id` | TEXT |
| `sender` | TEXT |
| `subject` | TEXT |
| `body` | TEXT |
| `received_at` | TEXT |

## employee_shifts

| Column | SQLite type |
|---|---|
| `shift_id` | TEXT |
| `employee_id` | TEXT |
| `start_at` | TEXT |
| `end_at` | TEXT |

## employees

| Column | SQLite type |
|---|---|
| `employee_id` | TEXT |
| `department_id` | TEXT |
| `role` | TEXT |
| `experience_months` | INTEGER |

## invoices

| Column | SQLite type |
|---|---|
| `invoice_id` | TEXT |
| `subscription_id` | TEXT |
| `issued_at` | TEXT |
| `amount` | INTEGER |
| `currency` | TEXT |

## organizations

| Column | SQLite type |
|---|---|
| `organization_id` | TEXT |
| `name` | TEXT |
| `segment` | TEXT |
| `region` | TEXT |

## payments

| Column | SQLite type |
|---|---|
| `payment_id` | TEXT |
| `invoice_id` | TEXT |
| `paid_at` | TEXT |
| `amount` | INTEGER |
| `status` | TEXT |

## product_releases

| Column | SQLite type |
|---|---|
| `release_id` | TEXT |
| `product_id` | TEXT |
| `released_at` | TEXT |
| `version` | TEXT |
| `release_type` | TEXT |

## products

| Column | SQLite type |
|---|---|
| `product_id` | TEXT |
| `name` | TEXT |

## refunds

| Column | SQLite type |
|---|---|
| `refund_id` | TEXT |
| `payment_id` | TEXT |
| `refunded_at` | TEXT |
| `amount` | INTEGER |
| `reason` | TEXT |

## routing_decisions

| Column | SQLite type |
|---|---|
| `decision_id` | TEXT |
| `ticket_id` | TEXT |
| `department_id` | TEXT |
| `decided_at` | TEXT |
| `decision_type` | TEXT |
| `actor_id` | TEXT |

## service_incidents

| Column | SQLite type |
|---|---|
| `incident_id` | TEXT |
| `product_id` | TEXT |
| `started_at` | TEXT |
| `ended_at` | TEXT |
| `kind` | TEXT |

## sla_policies

| Column | SQLite type |
|---|---|
| `sla_policy_id` | TEXT |
| `tier` | TEXT |
| `priority` | TEXT |
| `first_response_hours` | REAL |

## subscriptions

| Column | SQLite type |
|---|---|
| `subscription_id` | TEXT |
| `customer_id` | TEXT |
| `product_id` | TEXT |
| `tier` | TEXT |
| `started_at` | TEXT |

## ticket_assignments

| Column | SQLite type |
|---|---|
| `assignment_id` | TEXT |
| `ticket_id` | TEXT |
| `department_id` | TEXT |
| `assigned_at` | TEXT |

## ticket_events

| Column | SQLite type |
|---|---|
| `event_id` | TEXT |
| `ticket_id` | TEXT |
| `event_type` | TEXT |
| `occurred_at` | TEXT |
| `actor_id` | TEXT |

## ticket_messages

| Column | SQLite type |
|---|---|
| `message_id` | TEXT |
| `ticket_id` | TEXT |
| `created_at` | TEXT |
| `author_role` | TEXT |
| `body` | TEXT |

## tickets

| Column | SQLite type |
|---|---|
| `ticket_id` | TEXT |
| `customer_id` | TEXT |
| `organization_id` | TEXT |
| `subscription_id` | TEXT |
| `product_id` | TEXT |
| `created_at` | TEXT |
| `channel` | TEXT |
| `subject` | TEXT |
| `description` | TEXT |
| `sender` | TEXT |
| `language` | TEXT |
| `attachment_count` | INTEGER |
| `reported_urgency` | TEXT |
| `historical_department` | TEXT |
| `assigned_department_id` | TEXT |
| `assigned_employee_id` | TEXT |
| `status` | TEXT |
| `priority` | TEXT |
| `first_response_at` | TEXT |
| `resolved_at` | TEXT |
| `parent_ticket_id` | TEXT |
| `incident_id` | TEXT |
| `invoice_id` | TEXT |
| `sla_policy_id` | TEXT |

